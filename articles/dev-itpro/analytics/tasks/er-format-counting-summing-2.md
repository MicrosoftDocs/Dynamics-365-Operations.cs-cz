---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2 - Konfigurace výpočtů)
description: Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ef657b13bc1f7f4a84676821e4175ace32c069a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551292"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2-configure-computations"></a><span data-ttu-id="5afd9-103">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2: Konfigurace výpočtů)</span><span class="sxs-lookup"><span data-stu-id="5afd9-103">ER Configure format to do counting and summing (Part 2: Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5afd9-104">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="5afd9-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="5afd9-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="5afd9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="5afd9-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 1: Vytvoření formátu).</span><span class="sxs-lookup"><span data-stu-id="5afd9-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="5afd9-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="5afd9-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="5afd9-108">Vytvoření konfigurace formátu pro přidání podrobností o počítání a sčítání</span><span class="sxs-lookup"><span data-stu-id="5afd9-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="5afd9-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5afd9-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5afd9-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5afd9-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5afd9-111">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="5afd9-112">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="5afd9-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="5afd9-113">Předpokládejme třeba, že potřebujete přizpůsobit formát poskytovaný společností Microsoft přidáním řádků se souhrnnými údaji na konci sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="5afd9-114">Je třeba to provést odvozením vlastní instance konfigurace Intrastat z instance Microsoft k provádění změn.</span><span class="sxs-lookup"><span data-stu-id="5afd9-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="5afd9-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5afd9-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="5afd9-116">V poli Nový zadejte „Odvodit z názvu: Intrastat (DE), Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="5afd9-117">Do pole Název zadejte hodnotu Intrastat (DE) s výpočty a součty.</span><span class="sxs-lookup"><span data-stu-id="5afd9-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="5afd9-118">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="5afd9-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="5afd9-119">Konfigurace sestavy na provádění výpočtů a součtů na základě podrobností výstupu</span><span class="sxs-lookup"><span data-stu-id="5afd9-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="5afd9-120">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="5afd9-120">Click Designer.</span></span>
2. <span data-ttu-id="5afd9-121">Vyberte možnost Ano v poli Podrobnosti výstupu shromažďování.</span><span class="sxs-lookup"><span data-stu-id="5afd9-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="5afd9-122">Tento příznak bude při spuštění aktivovat proces shromažďování podrobnosti výstupu pro generování souboru Intrastat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="5afd9-123">Potřebujete provést výpočet pro různé pokyny Intrastat, takže přidejte vyhrazené vyčíslení modelu k seznamu zdrojů dat této konfigurace formátu.</span><span class="sxs-lookup"><span data-stu-id="5afd9-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="5afd9-124">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="5afd9-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="5afd9-125">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5afd9-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="5afd9-126">Ve stromovém zobrazení vyberte možnost Datový model\Výčet.</span><span class="sxs-lookup"><span data-stu-id="5afd9-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="5afd9-127">Do pole Název zadejte Směr.</span><span class="sxs-lookup"><span data-stu-id="5afd9-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="5afd9-128">V poli Výčet modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5afd9-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="5afd9-129">Vyberte hodnotu Směr.</span><span class="sxs-lookup"><span data-stu-id="5afd9-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="5afd9-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5afd9-130">Click OK.</span></span>
9. <span data-ttu-id="5afd9-131">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5afd9-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="5afd9-132">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="5afd9-133">Do pole Název zadejte '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="5afd9-134">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="5afd9-134">Click Edit formula.</span></span>
13. <span data-ttu-id="5afd9-135">Do pole Vzorec zadejte '"block"'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="5afd9-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-136">Click Save.</span></span>
15. <span data-ttu-id="5afd9-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-137">Close the page.</span></span>
16. <span data-ttu-id="5afd9-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5afd9-138">Click OK.</span></span>
17. <span data-ttu-id="5afd9-139">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5afd9-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="5afd9-140">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="5afd9-141">Do pole Název zadejte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="5afd9-142">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="5afd9-142">Click Edit formula.</span></span>
21. <span data-ttu-id="5afd9-143">Do pole Vzorec zadejte '"record"'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="5afd9-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-144">Click Save.</span></span>
23. <span data-ttu-id="5afd9-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-145">Close the page.</span></span>
24. <span data-ttu-id="5afd9-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5afd9-146">Click OK.</span></span>
25. <span data-ttu-id="5afd9-147">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5afd9-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="5afd9-148">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="5afd9-149">Do pole Název zadejte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="5afd9-150">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="5afd9-150">Click Edit formula.</span></span>
29. <span data-ttu-id="5afd9-151">Do pole Vzorec zadejte '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="5afd9-152">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-152">Click Save.</span></span>
31. <span data-ttu-id="5afd9-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-153">Close the page.</span></span>
32. <span data-ttu-id="5afd9-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5afd9-154">Click OK.</span></span>
33. <span data-ttu-id="5afd9-155">Ve stromovém zobrazení vyberte 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="5afd9-156">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"</span><span class="sxs-lookup"><span data-stu-id="5afd9-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="5afd9-157">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5afd9-157">Click Add data source.</span></span>
    * <span data-ttu-id="5afd9-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="5afd9-158">$BlockName</span></span>  
36. <span data-ttu-id="5afd9-159">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-159">Click Save.</span></span>
37. <span data-ttu-id="5afd9-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-160">Close the page.</span></span>
38. <span data-ttu-id="5afd9-161">Klepněte na tlačítko Upravit pro pole Hodnota klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="5afd9-162">Do pole Vzorec zadejte 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="5afd9-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="5afd9-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="5afd9-164">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-164">Click Save.</span></span>
41. <span data-ttu-id="5afd9-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-165">Close the page.</span></span>
    * <span data-ttu-id="5afd9-166">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="5afd9-166">Count the lines of this sequence.</span></span> <span data-ttu-id="5afd9-167">Výsledky budou použity s názvem blok nezávisle pro různé pokyny.</span><span class="sxs-lookup"><span data-stu-id="5afd9-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="5afd9-168">Hodnota "Import" se použije pro všechny příchozí transakce Intrastat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="5afd9-169">Hodnota "Export" se použije pro všechny odchozí transakce Intrastat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="5afd9-170">Zvažte použití virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="5afd9-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5afd9-171">Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export".</span><span class="sxs-lookup"><span data-stu-id="5afd9-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="5afd9-172">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="5afd9-173">Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Příjezdy?'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="5afd9-174">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat".</span><span class="sxs-lookup"><span data-stu-id="5afd9-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="5afd9-175">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="5afd9-175">Count the lines of this sequence.</span></span> <span data-ttu-id="5afd9-176">Výsledky budou uloženy do paměti s názvem "záznam".</span><span class="sxs-lookup"><span data-stu-id="5afd9-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="5afd9-177">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="5afd9-178">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5afd9-178">Click Add data source.</span></span>
47. <span data-ttu-id="5afd9-179">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-179">Click Save.</span></span>
48. <span data-ttu-id="5afd9-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-180">Close the page.</span></span>
49. <span data-ttu-id="5afd9-181">Klepněte na tlačítko Upravit pro pole Hodnota klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="5afd9-182">Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="5afd9-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="5afd9-183">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-183">Click Save.</span></span>
52. <span data-ttu-id="5afd9-184">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-184">Close the page.</span></span>
    * <span data-ttu-id="5afd9-185">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="5afd9-185">Count the lines of this sequence.</span></span> <span data-ttu-id="5afd9-186">Výsledky budou použity s názvem záznam nezávisle pro různé kódy komodit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="5afd9-187">Zvažte použití virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="5afd9-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="5afd9-188">Pro každou transakci použijte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export", a ve druhém záznamu bloku hodnota kódu komodity.</span><span class="sxs-lookup"><span data-stu-id="5afd9-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="5afd9-189">Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Expedice?'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="5afd9-190">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"</span><span class="sxs-lookup"><span data-stu-id="5afd9-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="5afd9-191">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="5afd9-192">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5afd9-192">Click Add data source.</span></span>
57. <span data-ttu-id="5afd9-193">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-193">Click Save.</span></span>
58. <span data-ttu-id="5afd9-194">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-194">Close the page.</span></span>
59. <span data-ttu-id="5afd9-195">Klepněte na tlačítko Upravit pro pole Hodnota klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="5afd9-196">Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="5afd9-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="5afd9-197">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-197">Click Save.</span></span>
62. <span data-ttu-id="5afd9-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-198">Close the page.</span></span>
63. <span data-ttu-id="5afd9-199">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="5afd9-200">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?\Záznam = Intrastat.CommodityRecord“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="5afd9-201">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="5afd9-201">Click the Format tab.</span></span>
66. <span data-ttu-id="5afd9-202">Ve stromové struktuře vyberte "Intrastat\Data\Expedice\Záznam\Částka faktury EUR".</span><span class="sxs-lookup"><span data-stu-id="5afd9-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="5afd9-203">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="5afd9-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="5afd9-204">Klepněte na tlačítko Upravit pro pole Název klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="5afd9-205">Ve stromovém zobrazení vyberte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="5afd9-206">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5afd9-206">Click Add data source.</span></span>
71. <span data-ttu-id="5afd9-207">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-207">Click Save.</span></span>
72. <span data-ttu-id="5afd9-208">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-208">Close the page.</span></span>
    * <span data-ttu-id="5afd9-209">Sečtěte hodnoty fakturované částky pro řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="5afd9-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="5afd9-210">Výsledky budou použity s názvem InvoicedAmountEUR nezávisle pro různé pokyny Intrastat a kódy komodit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="5afd9-211">Zvažte vytvoření virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="5afd9-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="5afd9-212">Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export".</span><span class="sxs-lookup"><span data-stu-id="5afd9-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="5afd9-213">Druhý blok "záznam" je vyplněn hodnotou kódu komodity a třetí sloupec, který "InvoicedAmountEUR" je vyplněn hodnotou částky faktury.</span><span class="sxs-lookup"><span data-stu-id="5afd9-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="5afd9-214">Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="5afd9-215">Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?\Záznam = Intrastat.CommodityRecord“.</span><span class="sxs-lookup"><span data-stu-id="5afd9-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="5afd9-216">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="5afd9-216">Click the Format tab.</span></span>
76. <span data-ttu-id="5afd9-217">Ve stromové struktuře vyberte "Intrastat\Data\Příjezdy\Záznam\Částka faktury EUR".</span><span class="sxs-lookup"><span data-stu-id="5afd9-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="5afd9-218">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="5afd9-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="5afd9-219">Klepněte na tlačítko Upravit pro pole Název klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="5afd9-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="5afd9-220">Ve stromovém zobrazení vyberte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="5afd9-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="5afd9-221">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5afd9-221">Click Add data source.</span></span>
81. <span data-ttu-id="5afd9-222">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-222">Click Save.</span></span>
82. <span data-ttu-id="5afd9-223">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-223">Close the page.</span></span>
83. <span data-ttu-id="5afd9-224">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5afd9-224">Click Save.</span></span>
84. <span data-ttu-id="5afd9-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5afd9-225">Close the page.</span></span>

