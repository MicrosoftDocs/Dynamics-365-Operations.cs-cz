---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3 - Použití výpočtů k vytvoření výstupu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 3)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748990"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="87a0c-104">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3 - Použití výpočtů k vytvoření výstupu)</span><span class="sxs-lookup"><span data-stu-id="87a0c-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="87a0c-105">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="87a0c-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="87a0c-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="87a0c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="87a0c-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 2: Konfigurace výpočtů).</span><span class="sxs-lookup"><span data-stu-id="87a0c-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="87a0c-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="87a0c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="87a0c-109">Konfigurace sestavy na používání informací o počítání a sčítání</span><span class="sxs-lookup"><span data-stu-id="87a0c-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="87a0c-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="87a0c-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="87a0c-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="87a0c-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="87a0c-112">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="87a0c-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="87a0c-113">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="87a0c-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="87a0c-114">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="87a0c-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="87a0c-115">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="87a0c-115">Click Designer.</span></span>
7. <span data-ttu-id="87a0c-116">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="87a0c-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="87a0c-117">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="87a0c-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="87a0c-118">Přidejte nový zdroj dat, abyste získali seznam bloků uložených do paměti.</span><span class="sxs-lookup"><span data-stu-id="87a0c-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="87a0c-119">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="87a0c-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="87a0c-120">Do pole Název zadejte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="87a0c-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="87a0c-121">$BlocksList</span></span>  
11. <span data-ttu-id="87a0c-122">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-122">Click Edit formula.</span></span>
12. <span data-ttu-id="87a0c-123">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="87a0c-124">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="87a0c-124">Click Add function.</span></span>
14. <span data-ttu-id="87a0c-125">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="87a0c-125">Click Add data source.</span></span>
15. <span data-ttu-id="87a0c-126">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="87a0c-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="87a0c-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="87a0c-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="87a0c-128">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="87a0c-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="87a0c-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="87a0c-130">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="87a0c-130">Click Save.</span></span>
    * <span data-ttu-id="87a0c-131">Vzorec "\*" znamená, že všechny bloky budou zahrnuty do seznamu pro tento záznam.</span><span class="sxs-lookup"><span data-stu-id="87a0c-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="87a0c-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-132">Close the page.</span></span>
19. <span data-ttu-id="87a0c-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87a0c-133">Click OK.</span></span>
20. <span data-ttu-id="87a0c-134">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="87a0c-134">Click the Format tab.</span></span>
21. <span data-ttu-id="87a0c-135">Ve stromovém zobrazení vyberte 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="87a0c-136">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="87a0c-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="87a0c-137">Ve stromovém zobrazení vyberte 'Text\Pořadí'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="87a0c-138">Do pole Název zadejte 'Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="87a0c-139">Součty podle bloků</span><span class="sxs-lookup"><span data-stu-id="87a0c-139">Totals by blocks</span></span>  
25. <span data-ttu-id="87a0c-140">V poli speciální znaky vyberte "Nový řádek – Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="87a0c-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="87a0c-141">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87a0c-141">Click OK.</span></span>
27. <span data-ttu-id="87a0c-142">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="87a0c-143">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="87a0c-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="87a0c-144">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="87a0c-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="87a0c-145">Do pole Název zadejte Kód bloku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="87a0c-146">Kód bloku</span><span class="sxs-lookup"><span data-stu-id="87a0c-146">Block code</span></span>  
31. <span data-ttu-id="87a0c-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87a0c-147">Click OK.</span></span>
32. <span data-ttu-id="87a0c-148">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-148">Click Add String.</span></span>
33. <span data-ttu-id="87a0c-149">Do pole Název zadejte Počítání řádků.</span><span class="sxs-lookup"><span data-stu-id="87a0c-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="87a0c-150">Počítání řádků</span><span class="sxs-lookup"><span data-stu-id="87a0c-150">Lines counting</span></span>  
34. <span data-ttu-id="87a0c-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87a0c-151">Click OK.</span></span>
35. <span data-ttu-id="87a0c-152">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-152">Click Add String.</span></span>
36. <span data-ttu-id="87a0c-153">Do pole Název zadejte „Celková částka“.</span><span class="sxs-lookup"><span data-stu-id="87a0c-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="87a0c-154">Celková částka</span><span class="sxs-lookup"><span data-stu-id="87a0c-154">Total amount</span></span>  
37. <span data-ttu-id="87a0c-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87a0c-155">Click OK.</span></span>
38. <span data-ttu-id="87a0c-156">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="87a0c-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="87a0c-157">Ve stromovém zobrazení vyberte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="87a0c-158">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="87a0c-158">Click Bind.</span></span>
    * <span data-ttu-id="87a0c-159">Vytvořte souhrnný řádek pro každý blok uložený do paměti.</span><span class="sxs-lookup"><span data-stu-id="87a0c-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="87a0c-160">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="87a0c-160">Click the Format tab.</span></span>
42. <span data-ttu-id="87a0c-161">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Kód bloku'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="87a0c-162">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="87a0c-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="87a0c-163">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-163">Click Edit formula.</span></span>
45. <span data-ttu-id="87a0c-164">Do pole Vzorec zadejte '"ID bloku: " & '.</span><span class="sxs-lookup"><span data-stu-id="87a0c-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="87a0c-165">"ID bloku: " &</span><span class="sxs-lookup"><span data-stu-id="87a0c-165">"Block id: " &</span></span>  
46. <span data-ttu-id="87a0c-166">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="87a0c-167">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="87a0c-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="87a0c-168">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="87a0c-168">Click Add data source.</span></span>
49. <span data-ttu-id="87a0c-169">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87a0c-169">Click Save.</span></span>
50. <span data-ttu-id="87a0c-170">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-170">Close the page.</span></span>
51. <span data-ttu-id="87a0c-171">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="87a0c-171">Click the Format tab.</span></span>
52. <span data-ttu-id="87a0c-172">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Počítání řádků'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="87a0c-173">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="87a0c-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="87a0c-174">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-174">Click Edit formula.</span></span>
    * <span data-ttu-id="87a0c-175">Vytvořte výstup pro počet řádků pro každý blok prezentovaný v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="87a0c-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="87a0c-176">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku:" & '.</span><span class="sxs-lookup"><span data-stu-id="87a0c-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="87a0c-177">"Počet řádků v tomto bloku: " &</span><span class="sxs-lookup"><span data-stu-id="87a0c-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="87a0c-178">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="87a0c-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="87a0c-179">"Počet řádků v tomto bloku: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="87a0c-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="87a0c-180">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="87a0c-181">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="87a0c-181">Click Add function.</span></span>
59. <span data-ttu-id="87a0c-182">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="87a0c-182">Click Add data source.</span></span>
60. <span data-ttu-id="87a0c-183">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="87a0c-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="87a0c-184">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="87a0c-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="87a0c-185">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="87a0c-186">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="87a0c-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="87a0c-187">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="87a0c-187">Click Add data source.</span></span>
64. <span data-ttu-id="87a0c-188">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="87a0c-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="87a0c-189">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="87a0c-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="87a0c-190">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="87a0c-191">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="87a0c-191">Click Add data source.</span></span>
67. <span data-ttu-id="87a0c-192">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="87a0c-193">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="87a0c-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="87a0c-194">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87a0c-194">Click Save.</span></span>
69. <span data-ttu-id="87a0c-195">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-195">Close the page.</span></span>
70. <span data-ttu-id="87a0c-196">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="87a0c-196">Click the Format tab.</span></span>
71. <span data-ttu-id="87a0c-197">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Celková částka'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="87a0c-198">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="87a0c-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="87a0c-199">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="87a0c-199">Click Edit formula.</span></span>
    * <span data-ttu-id="87a0c-200">Vytvořte výstup, který bude představovat součet fakturované částky pro každý blok v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="87a0c-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="87a0c-201">Do pole Vzorec zadejte '"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="87a0c-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="87a0c-202">"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="87a0c-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="87a0c-203">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87a0c-203">Click Save.</span></span>
76. <span data-ttu-id="87a0c-204">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-204">Close the page.</span></span>
77. <span data-ttu-id="87a0c-205">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87a0c-205">Click Save.</span></span>
78. <span data-ttu-id="87a0c-206">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="87a0c-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]