---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)
description: Toto téma popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092293"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="d74f6-104">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)</span><span class="sxs-lookup"><span data-stu-id="d74f6-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d74f6-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="d74f6-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d74f6-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="d74f6-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="d74f6-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").</span><span class="sxs-lookup"><span data-stu-id="d74f6-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="d74f6-108">Návrh sestavy k předložení finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="d74f6-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="d74f6-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="d74f6-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d74f6-110">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="d74f6-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d74f6-111">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="d74f6-112">V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".</span><span class="sxs-lookup"><span data-stu-id="d74f6-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="d74f6-113">Použijte model vytvořený předem jako zdroj dat pro novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="d74f6-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="d74f6-114">Do pole Název zadejte 'Sestava deníku hlavní knihy'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="d74f6-115">V poli Definice datového modelu vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="d74f6-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="d74f6-116">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="d74f6-116">Click Create configuration.</span></span>
8. <span data-ttu-id="d74f6-117">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="d74f6-117">Click Designer.</span></span>
9. <span data-ttu-id="d74f6-118">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="d74f6-119">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="d74f6-120">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="d74f6-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="d74f6-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-121">Click OK.</span></span>
13. <span data-ttu-id="d74f6-122">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="d74f6-123">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="d74f6-124">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="d74f6-125">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-125">Click OK.</span></span>
17. <span data-ttu-id="d74f6-126">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="d74f6-127">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="d74f6-128">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="d74f6-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="d74f6-129">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-129">Click OK.</span></span>
21. <span data-ttu-id="d74f6-130">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="d74f6-131">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="d74f6-132">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="d74f6-133">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="d74f6-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="d74f6-134">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-134">Click OK.</span></span>
26. <span data-ttu-id="d74f6-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="d74f6-136">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="d74f6-137">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="d74f6-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="d74f6-138">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-138">Click OK.</span></span>
30. <span data-ttu-id="d74f6-139">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="d74f6-140">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="d74f6-141">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="d74f6-142">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="d74f6-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="d74f6-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-143">Click OK.</span></span>
35. <span data-ttu-id="d74f6-144">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="d74f6-145">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="d74f6-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="d74f6-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-146">Click OK.</span></span>
38. <span data-ttu-id="d74f6-147">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="d74f6-148">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="d74f6-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="d74f6-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-149">Click OK.</span></span>
41. <span data-ttu-id="d74f6-150">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="d74f6-151">Do pole Název zadejte 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="d74f6-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-152">Click OK.</span></span>
44. <span data-ttu-id="d74f6-153">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="d74f6-154">Do pole název zadejte 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="d74f6-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-155">Click OK.</span></span>
47. <span data-ttu-id="d74f6-156">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="d74f6-157">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="d74f6-158">Do pole Název dimenze zadejte Dimenze.</span><span class="sxs-lookup"><span data-stu-id="d74f6-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="d74f6-159">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-159">Click OK.</span></span>
51. <span data-ttu-id="d74f6-160">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="d74f6-161">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="d74f6-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="d74f6-162">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="d74f6-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="d74f6-163">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="d74f6-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="d74f6-164">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-164">Click OK.</span></span>
56. <span data-ttu-id="d74f6-165">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="d74f6-166">Do pole Název zadejte Hodnota.</span><span class="sxs-lookup"><span data-stu-id="d74f6-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="d74f6-167">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-167">Click OK.</span></span>
59. <span data-ttu-id="d74f6-168">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="d74f6-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="d74f6-169">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="d74f6-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="d74f6-170">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d74f6-170">Click OK.</span></span>
<span data-ttu-id="d74f6-171">![Stránka návrháře operací ER](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="d74f6-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="d74f6-172">Mapování prvků sestavy na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="d74f6-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="d74f6-173">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="d74f6-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="d74f6-174">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="d74f6-175">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="d74f6-176">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="d74f6-177">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="d74f6-178">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="d74f6-179">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="d74f6-180">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-180">Click Bind.</span></span>
9. <span data-ttu-id="d74f6-181">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="d74f6-182">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="d74f6-183">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-183">Click Bind.</span></span>
12. <span data-ttu-id="d74f6-184">Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="d74f6-185">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="d74f6-186">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-186">Click Bind.</span></span>
15. <span data-ttu-id="d74f6-187">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="d74f6-188">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="d74f6-189">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-189">Click Bind.</span></span>
18. <span data-ttu-id="d74f6-190">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="d74f6-191">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="d74f6-192">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-192">Click Bind.</span></span>
21. <span data-ttu-id="d74f6-193">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="d74f6-194">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="d74f6-195">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-195">Click Bind.</span></span>
24. <span data-ttu-id="d74f6-196">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="d74f6-197">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="d74f6-198">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-198">Click Bind.</span></span>
27. <span data-ttu-id="d74f6-199">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="d74f6-200">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="d74f6-201">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-201">Click Bind.</span></span>
30. <span data-ttu-id="d74f6-202">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="d74f6-203">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="d74f6-204">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-204">Click Bind.</span></span>
33. <span data-ttu-id="d74f6-205">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="d74f6-206">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="d74f6-207">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-207">Click Bind.</span></span>
36. <span data-ttu-id="d74f6-208">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="d74f6-209">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="d74f6-210">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-210">Click Bind.</span></span>
39. <span data-ttu-id="d74f6-211">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="d74f6-212">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="d74f6-213">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-213">Click Bind.</span></span>
42. <span data-ttu-id="d74f6-214">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="d74f6-215">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="d74f6-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="d74f6-216">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="d74f6-216">Click Bind.</span></span>
45. <span data-ttu-id="d74f6-217">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="d74f6-217">Click Save.</span></span>
46. <span data-ttu-id="d74f6-218">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d74f6-218">Close the page.</span></span>
<span data-ttu-id="d74f6-219">![Stránka návrháře operací ER](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="d74f6-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

