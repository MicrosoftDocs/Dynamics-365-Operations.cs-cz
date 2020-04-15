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
ms.openlocfilehash: b89d08d8f6a4223eb592ffa2b918504839e5287b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142402"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="ef353-103">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="ef353-103">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef353-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="ef353-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ef353-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="ef353-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="ef353-106">K dokončení těchto kroků je nutné nejprve provést kroky v postupu „Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu)“.</span><span class="sxs-lookup"><span data-stu-id="ef353-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="ef353-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="ef353-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="ef353-108">Testování této konfigurace pro generování sestav Intrastat</span><span class="sxs-lookup"><span data-stu-id="ef353-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="ef353-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="ef353-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ef353-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="ef353-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ef353-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="ef353-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ef353-112">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ef353-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ef353-113">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ef353-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ef353-114">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="ef353-115">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ef353-115">Click User parameters.</span></span>
8. <span data-ttu-id="ef353-116">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="ef353-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="ef353-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef353-117">Click OK.</span></span>
10. <span data-ttu-id="ef353-118">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="ef353-118">Click Edit.</span></span>
11. <span data-ttu-id="ef353-119">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="ef353-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="ef353-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ef353-120">Click Save.</span></span>
13. <span data-ttu-id="ef353-121">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="ef353-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="ef353-122">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="ef353-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="ef353-123">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="ef353-123">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="ef353-124">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="ef353-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="ef353-125">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="ef353-125">Click Save.</span></span>
18. <span data-ttu-id="ef353-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef353-126">Close the page.</span></span>
19. <span data-ttu-id="ef353-127">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ef353-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="ef353-128">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="ef353-128">Click Output.</span></span>
21. <span data-ttu-id="ef353-129">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="ef353-129">Click Report.</span></span>
    * <span data-ttu-id="ef353-130">Spusťte proces generování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ef353-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="ef353-131">V poli Datum od nastavte datum a čas na „2000-01-01“ .</span><span class="sxs-lookup"><span data-stu-id="ef353-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="ef353-132">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="ef353-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="ef353-133">V poli Datum do nastavte datum a čas na „2022-12-31“ .</span><span class="sxs-lookup"><span data-stu-id="ef353-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="ef353-134">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="ef353-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="ef353-135">V poli Směr vyberte hodnotu Dovoz.</span><span class="sxs-lookup"><span data-stu-id="ef353-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="ef353-136">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="ef353-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="ef353-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef353-137">Click OK.</span></span>
    * <span data-ttu-id="ef353-138">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="ef353-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="ef353-139">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef353-139">Click New.</span></span>
28. <span data-ttu-id="ef353-140">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ef353-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="ef353-141">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="ef353-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="ef353-142">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef353-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="ef353-143">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef353-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="ef353-144">Nastavte hodnotu Váha na 10.</span><span class="sxs-lookup"><span data-stu-id="ef353-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="ef353-145">Nastavte hodnotu Částka k fakturaci na 10000.</span><span class="sxs-lookup"><span data-stu-id="ef353-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="ef353-146">Nastavte hodnotu Statistická částka na 10000.</span><span class="sxs-lookup"><span data-stu-id="ef353-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="ef353-147">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="ef353-147">Click Output.</span></span>
36. <span data-ttu-id="ef353-148">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="ef353-148">Click Report.</span></span>
37. <span data-ttu-id="ef353-149">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="ef353-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="ef353-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef353-150">Click OK.</span></span>
    * <span data-ttu-id="ef353-151">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="ef353-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="ef353-152">Všimněte si, že byl změněn ve srovnání s prvním spuštěním.</span><span class="sxs-lookup"><span data-stu-id="ef353-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="ef353-153">Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat</span><span class="sxs-lookup"><span data-stu-id="ef353-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="ef353-154">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ef353-155">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="ef353-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="ef353-156">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ef353-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="ef353-157">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ef353-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="ef353-158">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="ef353-159">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ef353-159">Click User parameters.</span></span>
7. <span data-ttu-id="ef353-160">Vyberte možnost Ano v poli Spustit v režimu ladění.</span><span class="sxs-lookup"><span data-stu-id="ef353-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="ef353-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef353-161">Click OK.</span></span>
9. <span data-ttu-id="ef353-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef353-162">Close the page.</span></span>
10. <span data-ttu-id="ef353-163">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="ef353-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="ef353-164">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="ef353-164">Click Output.</span></span>
12. <span data-ttu-id="ef353-165">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="ef353-165">Click Report.</span></span>
13. <span data-ttu-id="ef353-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef353-166">Click OK.</span></span>
14. <span data-ttu-id="ef353-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef353-167">Close the page.</span></span>
15. <span data-ttu-id="ef353-168">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="ef353-169">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="ef353-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="ef353-170">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="ef353-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="ef353-171">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="ef353-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="ef353-172">Klikněte na Protokoly ladění.</span><span class="sxs-lookup"><span data-stu-id="ef353-172">Click Debug logs.</span></span>
    * <span data-ttu-id="ef353-173">Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="ef353-174">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="ef353-174">Click Attach.</span></span>
21. <span data-ttu-id="ef353-175">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="ef353-175">Click Open.</span></span>
    * <span data-ttu-id="ef353-176">Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ef353-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

