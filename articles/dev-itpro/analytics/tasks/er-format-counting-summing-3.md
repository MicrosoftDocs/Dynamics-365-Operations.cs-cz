---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3 - Použití výpočtů k vytvoření výstupu)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544603"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="11512-103">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 3: Použití výpočtů k vytvoření výstupu)</span><span class="sxs-lookup"><span data-stu-id="11512-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="11512-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="11512-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="11512-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="11512-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="11512-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 2: Konfigurace výpočtů).</span><span class="sxs-lookup"><span data-stu-id="11512-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="11512-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="11512-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="11512-108">Konfigurace sestavy na používání informací o počítání a sčítání</span><span class="sxs-lookup"><span data-stu-id="11512-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="11512-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="11512-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="11512-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="11512-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="11512-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="11512-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="11512-112">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="11512-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="11512-113">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="11512-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="11512-114">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="11512-114">Click Designer.</span></span>
7. <span data-ttu-id="11512-115">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="11512-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="11512-116">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="11512-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="11512-117">Přidejte nový zdroj dat, abyste získali seznam bloků uložených do paměti.</span><span class="sxs-lookup"><span data-stu-id="11512-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="11512-118">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="11512-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="11512-119">Do pole Název zadejte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="11512-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="11512-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="11512-120">$BlocksList</span></span>  
11. <span data-ttu-id="11512-121">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="11512-121">Click Edit formula.</span></span>
12. <span data-ttu-id="11512-122">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="11512-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="11512-123">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="11512-123">Click Add function.</span></span>
14. <span data-ttu-id="11512-124">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="11512-124">Click Add data source.</span></span>
15. <span data-ttu-id="11512-125">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="11512-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="11512-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="11512-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="11512-127">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="11512-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="11512-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="11512-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="11512-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="11512-129">Click Save.</span></span>
    * <span data-ttu-id="11512-130">Vzorec "\*" znamená, že všechny bloky budou zahrnuty do seznamu pro tento záznam.</span><span class="sxs-lookup"><span data-stu-id="11512-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="11512-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11512-131">Close the page.</span></span>
19. <span data-ttu-id="11512-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="11512-132">Click OK.</span></span>
20. <span data-ttu-id="11512-133">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="11512-133">Click the Format tab.</span></span>
21. <span data-ttu-id="11512-134">Ve stromovém zobrazení vyberte 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="11512-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="11512-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="11512-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="11512-136">Ve stromovém zobrazení vyberte 'Text\Pořadí'.</span><span class="sxs-lookup"><span data-stu-id="11512-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="11512-137">Do pole Název zadejte 'Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="11512-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="11512-138">Součty podle bloků</span><span class="sxs-lookup"><span data-stu-id="11512-138">Totals by blocks</span></span>  
25. <span data-ttu-id="11512-139">V poli speciální znaky vyberte "Nový řádek – Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="11512-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="11512-140">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="11512-140">Click OK.</span></span>
27. <span data-ttu-id="11512-141">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="11512-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="11512-142">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="11512-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="11512-143">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="11512-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="11512-144">Do pole Název zadejte Kód bloku.</span><span class="sxs-lookup"><span data-stu-id="11512-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="11512-145">Kód bloku</span><span class="sxs-lookup"><span data-stu-id="11512-145">Block code</span></span>  
31. <span data-ttu-id="11512-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="11512-146">Click OK.</span></span>
32. <span data-ttu-id="11512-147">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="11512-147">Click Add String.</span></span>
33. <span data-ttu-id="11512-148">Do pole Název zadejte Počítání řádků.</span><span class="sxs-lookup"><span data-stu-id="11512-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="11512-149">Počítání řádků</span><span class="sxs-lookup"><span data-stu-id="11512-149">Lines counting</span></span>  
34. <span data-ttu-id="11512-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="11512-150">Click OK.</span></span>
35. <span data-ttu-id="11512-151">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="11512-151">Click Add String.</span></span>
36. <span data-ttu-id="11512-152">Do pole Název zadejte „Celková částka“.</span><span class="sxs-lookup"><span data-stu-id="11512-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="11512-153">Celková částka</span><span class="sxs-lookup"><span data-stu-id="11512-153">Total amount</span></span>  
37. <span data-ttu-id="11512-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="11512-154">Click OK.</span></span>
38. <span data-ttu-id="11512-155">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="11512-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="11512-156">Ve stromovém zobrazení vyberte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="11512-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="11512-157">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="11512-157">Click Bind.</span></span>
    * <span data-ttu-id="11512-158">Vytvořte souhrnný řádek pro každý blok uložený do paměti.</span><span class="sxs-lookup"><span data-stu-id="11512-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="11512-159">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="11512-159">Click the Format tab.</span></span>
42. <span data-ttu-id="11512-160">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Kód bloku'.</span><span class="sxs-lookup"><span data-stu-id="11512-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="11512-161">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="11512-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="11512-162">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="11512-162">Click Edit formula.</span></span>
45. <span data-ttu-id="11512-163">Do pole Vzorec zadejte '"ID bloku: " & '.</span><span class="sxs-lookup"><span data-stu-id="11512-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="11512-164">"ID bloku: " &</span><span class="sxs-lookup"><span data-stu-id="11512-164">"Block id: " &</span></span>  
46. <span data-ttu-id="11512-165">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="11512-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="11512-166">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="11512-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="11512-167">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="11512-167">Click Add data source.</span></span>
49. <span data-ttu-id="11512-168">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="11512-168">Click Save.</span></span>
50. <span data-ttu-id="11512-169">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11512-169">Close the page.</span></span>
51. <span data-ttu-id="11512-170">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="11512-170">Click the Format tab.</span></span>
52. <span data-ttu-id="11512-171">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Počítání řádků'.</span><span class="sxs-lookup"><span data-stu-id="11512-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="11512-172">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="11512-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="11512-173">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="11512-173">Click Edit formula.</span></span>
    * <span data-ttu-id="11512-174">Vytvořte výstup pro počet řádků pro každý blok prezentovaný v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="11512-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="11512-175">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku:" & '.</span><span class="sxs-lookup"><span data-stu-id="11512-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="11512-176">"Počet řádků v tomto bloku: " &</span><span class="sxs-lookup"><span data-stu-id="11512-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="11512-177">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="11512-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="11512-178">"Počet řádků v tomto bloku: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="11512-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="11512-179">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="11512-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="11512-180">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="11512-180">Click Add function.</span></span>
59. <span data-ttu-id="11512-181">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="11512-181">Click Add data source.</span></span>
60. <span data-ttu-id="11512-182">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="11512-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="11512-183">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="11512-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="11512-184">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="11512-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="11512-185">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="11512-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="11512-186">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="11512-186">Click Add data source.</span></span>
64. <span data-ttu-id="11512-187">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="11512-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="11512-188">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="11512-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="11512-189">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="11512-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="11512-190">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="11512-190">Click Add data source.</span></span>
67. <span data-ttu-id="11512-191">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="11512-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="11512-192">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="11512-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="11512-193">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="11512-193">Click Save.</span></span>
69. <span data-ttu-id="11512-194">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11512-194">Close the page.</span></span>
70. <span data-ttu-id="11512-195">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="11512-195">Click the Format tab.</span></span>
71. <span data-ttu-id="11512-196">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Celková částka'.</span><span class="sxs-lookup"><span data-stu-id="11512-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="11512-197">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="11512-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="11512-198">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="11512-198">Click Edit formula.</span></span>
    * <span data-ttu-id="11512-199">Vytvořte výstup, který bude představovat součet fakturované částky pro každý blok v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="11512-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="11512-200">Do pole Vzorec zadejte '"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span><span class="sxs-lookup"><span data-stu-id="11512-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="11512-201">"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="11512-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="11512-202">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="11512-202">Click Save.</span></span>
76. <span data-ttu-id="11512-203">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11512-203">Close the page.</span></span>
77. <span data-ttu-id="11512-204">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="11512-204">Click Save.</span></span>
78. <span data-ttu-id="11512-205">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11512-205">Close the page.</span></span>

