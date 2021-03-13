---
title: Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2 - Konfigurace výpočtů)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví tak, aby počítal a sčítal na základě dat již vygenerovaného textového výstupu. (část 2)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6215fe1f32bcb4833bd009b7c33e09edbba17817
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092990"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="4d1c6-104">Elektronické výkaznictví – konfigurace formátu počítání a sčítání (část 2 - Konfigurace výpočtů)</span><span class="sxs-lookup"><span data-stu-id="4d1c6-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d1c6-105">Následující procedura popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) k vytvoření počtu a součtu na základě dat již generovaného textového výstupu.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="4d1c6-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4d1c6-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Konfigurace formátu na provedení výpočtu a součtu (část 1: Vytvoření formátu).</span><span class="sxs-lookup"><span data-stu-id="4d1c6-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="4d1c6-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="4d1c6-109">Vytvoření konfigurace formátu pro přidání podrobností o počítání a sčítání</span><span class="sxs-lookup"><span data-stu-id="4d1c6-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="4d1c6-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4d1c6-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4d1c6-112">Ve stromovém zobrazení rozbalte „Modul Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="4d1c6-113">Ve stromové struktuře vyberte Modul Intrastat\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="4d1c6-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="4d1c6-114">Předpokládejme třeba, že potřebujete přizpůsobit formát poskytovaný společností Microsoft přidáním řádků se souhrnnými údaji na konci sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="4d1c6-115">Je třeba to provést odvozením vlastní instance konfigurace Intrastat z instance Microsoft k provádění změn.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="4d1c6-116">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="4d1c6-117">V poli Nový zadejte „Odvodit z názvu: Intrastat (DE), Microsoft“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="4d1c6-118">Do pole Název zadejte hodnotu Intrastat (DE) s výpočty a součty.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="4d1c6-119">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="4d1c6-120">Konfigurace sestavy na provádění výpočtů a součtů na základě podrobností výstupu</span><span class="sxs-lookup"><span data-stu-id="4d1c6-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="4d1c6-121">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-121">Click Designer.</span></span>
2. <span data-ttu-id="4d1c6-122">Vyberte možnost Ano v poli Podrobnosti výstupu shromažďování.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="4d1c6-123">Tento příznak bude při spuštění aktivovat proces shromažďování podrobnosti výstupu pro generování souboru Intrastat.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="4d1c6-124">Potřebujete provést výpočet pro různé pokyny Intrastat, takže přidejte vyhrazené vyčíslení modelu k seznamu zdrojů dat této konfigurace formátu.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="4d1c6-125">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="4d1c6-126">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="4d1c6-127">Ve stromovém zobrazení vyberte možnost Datový model\Výčet.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="4d1c6-128">Do pole Název zadejte Směr.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="4d1c6-129">V poli Výčet modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="4d1c6-130">Vyberte hodnotu Směr.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="4d1c6-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-131">Click OK.</span></span>
9. <span data-ttu-id="4d1c6-132">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="4d1c6-133">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="4d1c6-134">Do pole Název zadejte '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="4d1c6-135">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-135">Click Edit formula.</span></span>
13. <span data-ttu-id="4d1c6-136">Do pole Vzorec zadejte '"block"'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="4d1c6-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-137">Click Save.</span></span>
15. <span data-ttu-id="4d1c6-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-138">Close the page.</span></span>
16. <span data-ttu-id="4d1c6-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-139">Click OK.</span></span>
17. <span data-ttu-id="4d1c6-140">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="4d1c6-141">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="4d1c6-142">Do pole Název zadejte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="4d1c6-143">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-143">Click Edit formula.</span></span>
21. <span data-ttu-id="4d1c6-144">Do pole Vzorec zadejte '"record"'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="4d1c6-145">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-145">Click Save.</span></span>
23. <span data-ttu-id="4d1c6-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-146">Close the page.</span></span>
24. <span data-ttu-id="4d1c6-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-147">Click OK.</span></span>
25. <span data-ttu-id="4d1c6-148">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="4d1c6-149">Ve stromovém zobrazení vyberte možnost „Funkce\Počítané pole“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="4d1c6-150">Do pole Název zadejte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="4d1c6-151">Klikněte na možnost Upravit vzorec.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-151">Click Edit formula.</span></span>
29. <span data-ttu-id="4d1c6-152">Do pole Vzorec zadejte '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="4d1c6-153">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-153">Click Save.</span></span>
31. <span data-ttu-id="4d1c6-154">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-154">Close the page.</span></span>
32. <span data-ttu-id="4d1c6-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-155">Click OK.</span></span>
33. <span data-ttu-id="4d1c6-156">Ve stromovém zobrazení vyberte 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="4d1c6-157">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"</span><span class="sxs-lookup"><span data-stu-id="4d1c6-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="4d1c6-158">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-158">Click Add data source.</span></span>
    * <span data-ttu-id="4d1c6-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="4d1c6-159">$BlockName</span></span>  
36. <span data-ttu-id="4d1c6-160">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-160">Click Save.</span></span>
37. <span data-ttu-id="4d1c6-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-161">Close the page.</span></span>
38. <span data-ttu-id="4d1c6-162">Klepněte na tlačítko Upravit pro pole Hodnota klíče shromážděných dat.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="4d1c6-163">Do pole Vzorec zadejte 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="4d1c6-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="4d1c6-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="4d1c6-165">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-165">Click Save.</span></span>
41. <span data-ttu-id="4d1c6-166">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-166">Close the page.</span></span>
    * <span data-ttu-id="4d1c6-167">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-167">Count the lines of this sequence.</span></span> <span data-ttu-id="4d1c6-168">Výsledky budou použity s názvem "blok" nezávisle pro různé pokyny.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="4d1c6-169">Hodnota "Import" se použije pro všechny příchozí transakce Intrastat.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="4d1c6-170">Hodnota "Export" se použije pro všechny odchozí transakce Intrastat.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="4d1c6-171">Zvažte použití virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="4d1c6-172">Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="4d1c6-173">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="4d1c6-174">Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Příjezdy?'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="4d1c6-175">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="4d1c6-176">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-176">Count the lines of this sequence.</span></span> <span data-ttu-id="4d1c6-177">Výsledky budou uloženy do paměti s názvem "záznam".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="4d1c6-178">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="4d1c6-179">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-179">Click Add data source.</span></span>
47. <span data-ttu-id="4d1c6-180">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-180">Click Save.</span></span>
48. <span data-ttu-id="4d1c6-181">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-181">Close the page.</span></span>
49. <span data-ttu-id="4d1c6-182">Klepněte na tlačítko Upravit pro pole 'Hodnota klíče shromážděných dat'</span><span class="sxs-lookup"><span data-stu-id="4d1c6-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="4d1c6-183">Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="4d1c6-184">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-184">Click Save.</span></span>
52. <span data-ttu-id="4d1c6-185">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-185">Close the page.</span></span>
    * <span data-ttu-id="4d1c6-186">Spočítejte řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-186">Count the lines of this sequence.</span></span> <span data-ttu-id="4d1c6-187">Výsledky budou použity s názvem "záznam" nezávisle pro různé kódy komodit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="4d1c6-188">Zvažte použití virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="4d1c6-189">Pro každou transakci použijte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export", a ve druhém záznamu bloku hodnota kódu komodity.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="4d1c6-190">Ve stromovém zobrazení vyberte 'Intrastat\Data: Pořadí\Expedice?'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="4d1c6-191">Klepněte na tlačítko Upravit pro pole "Název klíče shromážděných dat"</span><span class="sxs-lookup"><span data-stu-id="4d1c6-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="4d1c6-192">Ve stromovém zobrazení vyberte '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="4d1c6-193">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-193">Click Add data source.</span></span>
57. <span data-ttu-id="4d1c6-194">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-194">Click Save.</span></span>
58. <span data-ttu-id="4d1c6-195">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-195">Close the page.</span></span>
59. <span data-ttu-id="4d1c6-196">Klepněte na tlačítko Upravit pro pole 'Hodnota klíče shromážděných dat'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="4d1c6-197">Do pole Vzorec zadejte "Intrastat.CommodityRecord.CommodityCode".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="4d1c6-198">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-198">Click Save.</span></span>
62. <span data-ttu-id="4d1c6-199">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-199">Close the page.</span></span>
63. <span data-ttu-id="4d1c6-200">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="4d1c6-201">Ve stromovém zobrazení rozbalte „Intrastat\Data: Pořadí\Expedice: Pořadí?\Záznam = Intrastat.CommodityRecord“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="4d1c6-202">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-202">Click the Format tab.</span></span>
66. <span data-ttu-id="4d1c6-203">Ve stromové struktuře vyberte "Intrastat\Data\Expedice\Záznam\Částka faktury EUR".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="4d1c6-204">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="4d1c6-205">Klepněte na tlačítko Upravit pro pole 'Název klíče shromážděných dat'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="4d1c6-206">Ve stromovém zobrazení vyberte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="4d1c6-207">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-207">Click Add data source.</span></span>
71. <span data-ttu-id="4d1c6-208">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-208">Click Save.</span></span>
72. <span data-ttu-id="4d1c6-209">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-209">Close the page.</span></span>
    * <span data-ttu-id="4d1c6-210">Sečtěte hodnoty fakturované částky pro řádky této sekvence.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="4d1c6-211">Výsledky budou použity s názvem "InvoicedAmountEUR" nezávisle pro různé pokyny Intrastat a kódy komodit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="4d1c6-212">Zvažte vytvoření virtuální tabulky aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="4d1c6-213">Pro každou transakci vytvořte řádek, kde jsou v prvním sloupci "blok" zadány příslušné hodnoty "Import" a "Export".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="4d1c6-214">Druhý blok "záznam" je vyplněn hodnotou kódu komodity a třetí sloupec, který "InvoicedAmountEUR" je vyplněn hodnotou částky faktury.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="4d1c6-215">Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="4d1c6-216">Ve stromovém zobrazení rozbalte „Intrastat\Data\Příjezdy?\Záznam = Intrastat.CommodityRecord“.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="4d1c6-217">Klikněte na kartu Formát.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-217">Click the Format tab.</span></span>
76. <span data-ttu-id="4d1c6-218">Ve stromové struktuře vyberte "Intrastat\Data\Příjezdy\Záznam\Částka faktury EUR".</span><span class="sxs-lookup"><span data-stu-id="4d1c6-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="4d1c6-219">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="4d1c6-220">Klepněte na tlačítko Upravit pro pole 'Název klíče shromážděných dat'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="4d1c6-221">Ve stromovém zobrazení vyberte '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="4d1c6-222">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-222">Click Add data source.</span></span>
81. <span data-ttu-id="4d1c6-223">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-223">Click Save.</span></span>
82. <span data-ttu-id="4d1c6-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-224">Close the page.</span></span>
83. <span data-ttu-id="4d1c6-225">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-225">Click Save.</span></span>
84. <span data-ttu-id="4d1c6-226">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4d1c6-226">Close the page.</span></span>

