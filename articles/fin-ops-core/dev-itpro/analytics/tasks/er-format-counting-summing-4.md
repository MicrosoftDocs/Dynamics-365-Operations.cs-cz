---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 4)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092940"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="cda31-104">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 4 - Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="cda31-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cda31-105">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="cda31-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="cda31-106">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="cda31-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="cda31-107">K dokončení těchto kroků je nutné nejprve provést kroky v postupu „Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 3: Používání výpočtů k vytvoření výstupu)“.</span><span class="sxs-lookup"><span data-stu-id="cda31-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="cda31-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="cda31-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="cda31-109">Testování této konfigurace pro generování sestav Intrastat</span><span class="sxs-lookup"><span data-stu-id="cda31-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="cda31-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cda31-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cda31-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cda31-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cda31-112">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="cda31-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="cda31-113">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="cda31-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="cda31-114">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="cda31-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="cda31-115">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="cda31-116">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="cda31-116">Click User parameters.</span></span>
8. <span data-ttu-id="cda31-117">Vyberte možnost Ano v poli Nastavení běhu.</span><span class="sxs-lookup"><span data-stu-id="cda31-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="cda31-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cda31-118">Click OK.</span></span>
10. <span data-ttu-id="cda31-119">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="cda31-119">Click Edit.</span></span>
11. <span data-ttu-id="cda31-120">Vyberte možnost Ano v poli Koncept běhu.</span><span class="sxs-lookup"><span data-stu-id="cda31-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="cda31-121">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cda31-121">Click Save.</span></span>
13. <span data-ttu-id="cda31-122">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="cda31-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="cda31-123">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cda31-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="cda31-124">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="cda31-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="cda31-125">Zvolte konfiguraci „Intrastat (DE) s výpočty a součty“.</span><span class="sxs-lookup"><span data-stu-id="cda31-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="cda31-126">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="cda31-126">Click Save.</span></span>
18. <span data-ttu-id="cda31-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cda31-127">Close the page.</span></span>
19. <span data-ttu-id="cda31-128">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="cda31-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="cda31-129">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="cda31-129">Click Output.</span></span>
21. <span data-ttu-id="cda31-130">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="cda31-130">Click Report.</span></span>
    * <span data-ttu-id="cda31-131">Spusťte proces generování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="cda31-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="cda31-132">V poli Datum od nastavte datum a čas na „2000-01-01“ .</span><span class="sxs-lookup"><span data-stu-id="cda31-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="cda31-133">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="cda31-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="cda31-134">V poli Datum do nastavte datum a čas na „2022-12-31“ .</span><span class="sxs-lookup"><span data-stu-id="cda31-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="cda31-135">Definujte počáteční a koncové datum pro období vykazování, které zahrnuje existující transakce formuláře.</span><span class="sxs-lookup"><span data-stu-id="cda31-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="cda31-136">V poli Směr vyberte hodnotu Dovoz.</span><span class="sxs-lookup"><span data-stu-id="cda31-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="cda31-137">Vyberte možnost Ano v poli Generovat soubor.</span><span class="sxs-lookup"><span data-stu-id="cda31-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="cda31-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cda31-138">Click OK.</span></span>
    * <span data-ttu-id="cda31-139">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="cda31-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="cda31-140">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cda31-140">Click New.</span></span>
28. <span data-ttu-id="cda31-141">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cda31-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="cda31-142">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="cda31-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="cda31-143">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cda31-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="cda31-144">V poli Komodita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cda31-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="cda31-145">Nastavte hodnotu Váha na 10.</span><span class="sxs-lookup"><span data-stu-id="cda31-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="cda31-146">Nastavte hodnotu Částka k fakturaci na 10000.</span><span class="sxs-lookup"><span data-stu-id="cda31-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="cda31-147">Nastavte hodnotu Statistická částka na 10000.</span><span class="sxs-lookup"><span data-stu-id="cda31-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="cda31-148">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="cda31-148">Click Output.</span></span>
36. <span data-ttu-id="cda31-149">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="cda31-149">Click Report.</span></span>
37. <span data-ttu-id="cda31-150">V poli Směr vyberte hodnotu Expedice.</span><span class="sxs-lookup"><span data-stu-id="cda31-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="cda31-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cda31-151">Click OK.</span></span>
    * <span data-ttu-id="cda31-152">Prohlédněte si vytvořený výstup souhrnných řádků v databázi.</span><span class="sxs-lookup"><span data-stu-id="cda31-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="cda31-153">Všimněte si, že byl změněn ve srovnání s prvním spuštěním.</span><span class="sxs-lookup"><span data-stu-id="cda31-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="cda31-154">Spuštění této konfigurace v režimu ladění ke kontrole společného počítání a sčítání dat</span><span class="sxs-lookup"><span data-stu-id="cda31-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="cda31-155">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="cda31-156">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="cda31-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="cda31-157">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="cda31-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="cda31-158">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="cda31-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="cda31-159">V podokně akcí klikněte na možnost Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="cda31-160">Klikněte na Parametry uživatelů.</span><span class="sxs-lookup"><span data-stu-id="cda31-160">Click User parameters.</span></span>
7. <span data-ttu-id="cda31-161">Vyberte možnost Ano v poli Spustit v režimu ladění.</span><span class="sxs-lookup"><span data-stu-id="cda31-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="cda31-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cda31-162">Click OK.</span></span>
9. <span data-ttu-id="cda31-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cda31-163">Close the page.</span></span>
10. <span data-ttu-id="cda31-164">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="cda31-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="cda31-165">Klepněte na Výstup.</span><span class="sxs-lookup"><span data-stu-id="cda31-165">Click Output.</span></span>
12. <span data-ttu-id="cda31-166">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="cda31-166">Click Report.</span></span>
13. <span data-ttu-id="cda31-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cda31-167">Click OK.</span></span>
14. <span data-ttu-id="cda31-168">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cda31-168">Close the page.</span></span>
15. <span data-ttu-id="cda31-169">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="cda31-170">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="cda31-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="cda31-171">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="cda31-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="cda31-172">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="cda31-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="cda31-173">Klikněte na Protokoly ladění.</span><span class="sxs-lookup"><span data-stu-id="cda31-173">Click Debug logs.</span></span>
    * <span data-ttu-id="cda31-174">Všimněte si, že záznam protokolu ladění byl vytvořen pro proces spuštění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="cda31-175">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="cda31-175">Click Attach.</span></span>
21. <span data-ttu-id="cda31-176">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="cda31-176">Click Open.</span></span>
    * <span data-ttu-id="cda31-177">Zkontrolujte vytvořený soubor XML, který obsahuje podrobnosti o počítání a sčítání, které byly shromážděny během provádění vybrané konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cda31-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

