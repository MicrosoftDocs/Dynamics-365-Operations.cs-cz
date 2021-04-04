---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)
description: Toto téma popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565231"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="12668-104">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)</span><span class="sxs-lookup"><span data-stu-id="12668-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12668-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="12668-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="12668-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="12668-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="12668-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").</span><span class="sxs-lookup"><span data-stu-id="12668-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="12668-108">Návrh sestavy k předložení finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="12668-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="12668-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="12668-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="12668-110">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="12668-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="12668-111">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="12668-112">V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".</span><span class="sxs-lookup"><span data-stu-id="12668-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="12668-113">Použijte model vytvořený předem jako zdroj dat pro novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="12668-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="12668-114">Do pole Název zadejte 'Sestava deníku hlavní knihy'.</span><span class="sxs-lookup"><span data-stu-id="12668-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="12668-115">V poli Definice datového modelu vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="12668-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="12668-116">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="12668-116">Click Create configuration.</span></span>
8. <span data-ttu-id="12668-117">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="12668-117">Click Designer.</span></span>
9. <span data-ttu-id="12668-118">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="12668-119">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="12668-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="12668-120">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="12668-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="12668-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-121">Click OK.</span></span>
13. <span data-ttu-id="12668-122">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="12668-123">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="12668-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="12668-124">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="12668-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="12668-125">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-125">Click OK.</span></span>
17. <span data-ttu-id="12668-126">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="12668-127">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="12668-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="12668-128">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="12668-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="12668-129">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-129">Click OK.</span></span>
21. <span data-ttu-id="12668-130">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="12668-131">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="12668-132">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="12668-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="12668-133">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="12668-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="12668-134">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-134">Click OK.</span></span>
26. <span data-ttu-id="12668-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="12668-136">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="12668-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="12668-137">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="12668-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="12668-138">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-138">Click OK.</span></span>
30. <span data-ttu-id="12668-139">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="12668-140">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="12668-141">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="12668-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="12668-142">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="12668-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="12668-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-143">Click OK.</span></span>
35. <span data-ttu-id="12668-144">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="12668-145">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="12668-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="12668-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-146">Click OK.</span></span>
38. <span data-ttu-id="12668-147">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="12668-148">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="12668-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="12668-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-149">Click OK.</span></span>
41. <span data-ttu-id="12668-150">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="12668-151">Do pole Název zadejte 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="12668-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="12668-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-152">Click OK.</span></span>
44. <span data-ttu-id="12668-153">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="12668-154">Do pole název zadejte 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="12668-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="12668-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-155">Click OK.</span></span>
47. <span data-ttu-id="12668-156">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="12668-157">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="12668-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="12668-158">Do pole Název dimenze zadejte Dimenze.</span><span class="sxs-lookup"><span data-stu-id="12668-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="12668-159">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-159">Click OK.</span></span>
51. <span data-ttu-id="12668-160">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="12668-161">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="12668-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="12668-162">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="12668-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="12668-163">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="12668-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="12668-164">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-164">Click OK.</span></span>
56. <span data-ttu-id="12668-165">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="12668-166">Do pole Název zadejte Hodnota.</span><span class="sxs-lookup"><span data-stu-id="12668-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="12668-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-167">Click OK.</span></span>
59. <span data-ttu-id="12668-168">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="12668-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="12668-169">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="12668-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="12668-170">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="12668-170">Click OK.</span></span>
<span data-ttu-id="12668-171">![Stránka návrháře operací ER](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="12668-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="12668-172">Mapování prvků sestavy na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="12668-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="12668-173">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="12668-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="12668-174">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.</span><span class="sxs-lookup"><span data-stu-id="12668-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="12668-175">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="12668-176">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="12668-177">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="12668-178">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="12668-179">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="12668-180">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-180">Click Bind.</span></span>
9. <span data-ttu-id="12668-181">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="12668-182">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="12668-183">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-183">Click Bind.</span></span>
12. <span data-ttu-id="12668-184">Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="12668-185">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="12668-186">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-186">Click Bind.</span></span>
15. <span data-ttu-id="12668-187">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="12668-188">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="12668-189">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-189">Click Bind.</span></span>
18. <span data-ttu-id="12668-190">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="12668-191">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="12668-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="12668-192">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-192">Click Bind.</span></span>
21. <span data-ttu-id="12668-193">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="12668-194">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="12668-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="12668-195">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-195">Click Bind.</span></span>
24. <span data-ttu-id="12668-196">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="12668-197">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="12668-198">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-198">Click Bind.</span></span>
27. <span data-ttu-id="12668-199">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="12668-200">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="12668-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="12668-201">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-201">Click Bind.</span></span>
30. <span data-ttu-id="12668-202">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="12668-203">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="12668-204">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-204">Click Bind.</span></span>
33. <span data-ttu-id="12668-205">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="12668-206">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="12668-207">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-207">Click Bind.</span></span>
36. <span data-ttu-id="12668-208">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="12668-209">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="12668-210">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-210">Click Bind.</span></span>
39. <span data-ttu-id="12668-211">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="12668-212">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="12668-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="12668-213">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-213">Click Bind.</span></span>
42. <span data-ttu-id="12668-214">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="12668-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="12668-215">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="12668-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="12668-216">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="12668-216">Click Bind.</span></span>
45. <span data-ttu-id="12668-217">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="12668-217">Click Save.</span></span>
46. <span data-ttu-id="12668-218">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="12668-218">Close the page.</span></span>
<span data-ttu-id="12668-219">![Stránka návrháře operací ER](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="12668-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]