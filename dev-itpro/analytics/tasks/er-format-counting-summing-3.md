--- 
title: "Použití výpočtů pro provádění výstupu počítání a sčítání pro elektronické výkaznictví (ER)"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 121f00efea6aee8d9df45d67f8f252bbf6b97176
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="8ec08-103">Použití výpočtů pro provádění výstupu počítání a sčítání pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="8ec08-103">Use computations to make the output for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ec08-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="8ec08-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="8ec08-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="8ec08-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="8ec08-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 2: Konfigurace výpočtů).</span><span class="sxs-lookup"><span data-stu-id="8ec08-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="8ec08-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="8ec08-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="8ec08-108">Konfigurace sestavy na používání informací o počítání a sčítání</span><span class="sxs-lookup"><span data-stu-id="8ec08-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="8ec08-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8ec08-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="8ec08-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="8ec08-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="8ec08-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="8ec08-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="8ec08-112">Ve stromovém zobrazení rozbalte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="8ec08-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="8ec08-113">Ve stromovém zobrazení vyberte 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing.</span><span class="sxs-lookup"><span data-stu-id="8ec08-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="8ec08-114">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="8ec08-114">Click Designer.</span></span>
7. <span data-ttu-id="8ec08-115">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="8ec08-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="8ec08-116">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8ec08-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="8ec08-117">Přidejte nový zdroj dat, abyste získali seznam bloků uložených do paměti.</span><span class="sxs-lookup"><span data-stu-id="8ec08-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="8ec08-118">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="8ec08-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="8ec08-119">Do pole Název zadejte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="8ec08-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="8ec08-120">$BlocksList</span></span>  
11. <span data-ttu-id="8ec08-121">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-121">Click Edit formula.</span></span>
12. <span data-ttu-id="8ec08-122">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="8ec08-123">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="8ec08-123">Click Add function.</span></span>
14. <span data-ttu-id="8ec08-124">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="8ec08-124">Click Add data source.</span></span>
15. <span data-ttu-id="8ec08-125">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="8ec08-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="8ec08-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="8ec08-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="8ec08-127">Do pole Vzorec zadejte 'COLLECTEDLIST('$BlockName', "*")'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "*")'.</span></span>
    * <span data-ttu-id="8ec08-128">COLLECTEDLIST('$BlockName', "*")</span><span class="sxs-lookup"><span data-stu-id="8ec08-128">COLLECTEDLIST('$BlockName', "*")</span></span>  
17. <span data-ttu-id="8ec08-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8ec08-129">Click Save.</span></span>
    * <span data-ttu-id="8ec08-130">Vzorec "*" znamená, že všechny bloky budou zahrnuty do seznamu pro tento záznam.</span><span class="sxs-lookup"><span data-stu-id="8ec08-130">The pattern “*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="8ec08-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-131">Close the page.</span></span>
19. <span data-ttu-id="8ec08-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8ec08-132">Click OK.</span></span>
20. <span data-ttu-id="8ec08-133">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="8ec08-133">Click the Format tab.</span></span>
21. <span data-ttu-id="8ec08-134">Ve stromovém zobrazení vyberte 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="8ec08-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8ec08-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="8ec08-136">Ve stromovém zobrazení vyberte 'Text\Pořadí'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="8ec08-137">Do pole Název zadejte 'Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="8ec08-138">Součty podle bloků</span><span class="sxs-lookup"><span data-stu-id="8ec08-138">Totals by blocks</span></span>  
25. <span data-ttu-id="8ec08-139">V poli speciální znaky vyberte "Nový řádek – Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="8ec08-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="8ec08-140">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8ec08-140">Click OK.</span></span>
27. <span data-ttu-id="8ec08-141">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="8ec08-142">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8ec08-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="8ec08-143">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="8ec08-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="8ec08-144">Do pole Název zadejte Kód bloku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="8ec08-145">Kód bloku</span><span class="sxs-lookup"><span data-stu-id="8ec08-145">Block code</span></span>  
31. <span data-ttu-id="8ec08-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8ec08-146">Click OK.</span></span>
32. <span data-ttu-id="8ec08-147">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-147">Click Add String.</span></span>
33. <span data-ttu-id="8ec08-148">Do pole Název zadejte Počítání řádků.</span><span class="sxs-lookup"><span data-stu-id="8ec08-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="8ec08-149">Počítání řádků</span><span class="sxs-lookup"><span data-stu-id="8ec08-149">Lines counting</span></span>  
34. <span data-ttu-id="8ec08-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8ec08-150">Click OK.</span></span>
35. <span data-ttu-id="8ec08-151">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-151">Click Add String.</span></span>
36. <span data-ttu-id="8ec08-152">Do pole Název zadejte „Celková částka“.</span><span class="sxs-lookup"><span data-stu-id="8ec08-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="8ec08-153">Celková částka</span><span class="sxs-lookup"><span data-stu-id="8ec08-153">Total amount</span></span>  
37. <span data-ttu-id="8ec08-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8ec08-154">Click OK.</span></span>
38. <span data-ttu-id="8ec08-155">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="8ec08-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="8ec08-156">Ve stromovém zobrazení vyberte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="8ec08-157">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="8ec08-157">Click Bind.</span></span>
    * <span data-ttu-id="8ec08-158">Vytvořte souhrnný řádek pro každý blok uložený do paměti.</span><span class="sxs-lookup"><span data-stu-id="8ec08-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="8ec08-159">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="8ec08-159">Click the Format tab.</span></span>
42. <span data-ttu-id="8ec08-160">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Kód bloku'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="8ec08-161">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="8ec08-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="8ec08-162">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-162">Click Edit formula.</span></span>
45. <span data-ttu-id="8ec08-163">Do pole Vzorec zadejte '"ID bloku: " & '.</span><span class="sxs-lookup"><span data-stu-id="8ec08-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="8ec08-164">"ID bloku: " &</span><span class="sxs-lookup"><span data-stu-id="8ec08-164">"Block id: " &</span></span>  
46. <span data-ttu-id="8ec08-165">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="8ec08-166">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="8ec08-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="8ec08-167">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="8ec08-167">Click Add data source.</span></span>
49. <span data-ttu-id="8ec08-168">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8ec08-168">Click Save.</span></span>
50. <span data-ttu-id="8ec08-169">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-169">Close the page.</span></span>
51. <span data-ttu-id="8ec08-170">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="8ec08-170">Click the Format tab.</span></span>
52. <span data-ttu-id="8ec08-171">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Počítání řádků'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="8ec08-172">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="8ec08-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="8ec08-173">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-173">Click Edit formula.</span></span>
    * <span data-ttu-id="8ec08-174">Vytvořte výstup pro počet řádků pro každý blok prezentovaný v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="8ec08-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="8ec08-175">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku:" & '.</span><span class="sxs-lookup"><span data-stu-id="8ec08-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="8ec08-176">"Počet řádků v tomto bloku: " &</span><span class="sxs-lookup"><span data-stu-id="8ec08-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="8ec08-177">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT('.</span><span class="sxs-lookup"><span data-stu-id="8ec08-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="8ec08-178">"Počet řádků v tomto bloku: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="8ec08-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="8ec08-179">Ve stromovém zobrazení vyberte 'Funkce shromažďování dat\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="8ec08-180">Klikněte na možnost Přidat funkci.</span><span class="sxs-lookup"><span data-stu-id="8ec08-180">Click Add function.</span></span>
59. <span data-ttu-id="8ec08-181">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="8ec08-181">Click Add data source.</span></span>
60. <span data-ttu-id="8ec08-182">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="8ec08-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="8ec08-183">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="8ec08-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="8ec08-184">Ve stromovém zobrazení rozbalte '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="8ec08-185">Ve stromovém zobrazení vyberte '$BlocksList\Hodnota'</span><span class="sxs-lookup"><span data-stu-id="8ec08-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="8ec08-186">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="8ec08-186">Click Add data source.</span></span>
64. <span data-ttu-id="8ec08-187">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span><span class="sxs-lookup"><span data-stu-id="8ec08-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="8ec08-188">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="8ec08-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="8ec08-189">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="8ec08-190">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="8ec08-190">Click Add data source.</span></span>
67. <span data-ttu-id="8ec08-191">V poli Vzorec zadejte hodnotu '"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="8ec08-192">"Počet řádků v tomto bloku: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="8ec08-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
68. <span data-ttu-id="8ec08-193">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8ec08-193">Click Save.</span></span>
69. <span data-ttu-id="8ec08-194">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-194">Close the page.</span></span>
70. <span data-ttu-id="8ec08-195">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="8ec08-195">Click the Format tab.</span></span>
71. <span data-ttu-id="8ec08-196">Ve stromovém zobrazení vyberte 'Intrastat\Data\Součty podle bloků\Celková částka'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="8ec08-197">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="8ec08-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="8ec08-198">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="8ec08-198">Click Edit formula.</span></span>
    * <span data-ttu-id="8ec08-199">Vytvořte výstup, který bude představovat součet fakturované částky pro každý blok v této sestavě.</span><span class="sxs-lookup"><span data-stu-id="8ec08-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="8ec08-200">Do pole Vzorec zadejte '"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span><span class="sxs-lookup"><span data-stu-id="8ec08-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))'.</span></span>
    * <span data-ttu-id="8ec08-201">"Součet fakturovaných částek: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span><span class="sxs-lookup"><span data-stu-id="8ec08-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))</span></span>  
75. <span data-ttu-id="8ec08-202">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8ec08-202">Click Save.</span></span>
76. <span data-ttu-id="8ec08-203">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-203">Close the page.</span></span>
77. <span data-ttu-id="8ec08-204">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8ec08-204">Click Save.</span></span>
78. <span data-ttu-id="8ec08-205">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ec08-205">Close the page.</span></span>


