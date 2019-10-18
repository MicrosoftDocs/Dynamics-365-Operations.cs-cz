---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 29dcf008f342603615241ab75860893cadc2b69e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182432"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3-design-the-report"></a><span data-ttu-id="b6040-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3: návrh sestavy)</span><span class="sxs-lookup"><span data-stu-id="b6040-103">ER Use financial dimensions as a data source (Part 3: Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6040-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b6040-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b6040-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="b6040-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b6040-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").</span><span class="sxs-lookup"><span data-stu-id="b6040-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="b6040-107">Návrh sestavy k předložení finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="b6040-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="b6040-108">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="b6040-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b6040-109">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b6040-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b6040-110">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b6040-111">V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".</span><span class="sxs-lookup"><span data-stu-id="b6040-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="b6040-112">Použijte model vytvořený předem jako zdroj dat pro novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="b6040-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="b6040-113">Do pole Název zadejte 'Sestava deníku hlavní knihy'.</span><span class="sxs-lookup"><span data-stu-id="b6040-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="b6040-114">V poli Definice datového modelu vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="b6040-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="b6040-115">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="b6040-115">Click Create configuration.</span></span>
8. <span data-ttu-id="b6040-116">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="b6040-116">Click Designer.</span></span>
9. <span data-ttu-id="b6040-117">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="b6040-118">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="b6040-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="b6040-119">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="b6040-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="b6040-120">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-120">Click OK.</span></span>
13. <span data-ttu-id="b6040-121">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="b6040-122">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="b6040-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="b6040-123">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="b6040-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="b6040-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-124">Click OK.</span></span>
17. <span data-ttu-id="b6040-125">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="b6040-126">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="b6040-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="b6040-127">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="b6040-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="b6040-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-128">Click OK.</span></span>
21. <span data-ttu-id="b6040-129">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="b6040-130">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="b6040-131">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="b6040-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="b6040-132">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="b6040-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="b6040-133">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-133">Click OK.</span></span>
26. <span data-ttu-id="b6040-134">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="b6040-135">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="b6040-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="b6040-136">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="b6040-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="b6040-137">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-137">Click OK.</span></span>
30. <span data-ttu-id="b6040-138">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="b6040-139">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="b6040-140">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="b6040-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="b6040-141">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="b6040-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="b6040-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-142">Click OK.</span></span>
35. <span data-ttu-id="b6040-143">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="b6040-144">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="b6040-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="b6040-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-145">Click OK.</span></span>
38. <span data-ttu-id="b6040-146">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="b6040-147">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="b6040-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="b6040-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-148">Click OK.</span></span>
41. <span data-ttu-id="b6040-149">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="b6040-150">Do pole Název zadejte 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="b6040-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="b6040-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-151">Click OK.</span></span>
44. <span data-ttu-id="b6040-152">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="b6040-153">Do pole název zadejte 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="b6040-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="b6040-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-154">Click OK.</span></span>
47. <span data-ttu-id="b6040-155">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="b6040-156">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="b6040-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="b6040-157">Do pole Název dimenze zadejte Dimenze.</span><span class="sxs-lookup"><span data-stu-id="b6040-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="b6040-158">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-158">Click OK.</span></span>
51. <span data-ttu-id="b6040-159">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="b6040-160">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b6040-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="b6040-161">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="b6040-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="b6040-162">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="b6040-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="b6040-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-163">Click OK.</span></span>
56. <span data-ttu-id="b6040-164">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="b6040-165">Do pole Název zadejte Hodnota.</span><span class="sxs-lookup"><span data-stu-id="b6040-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="b6040-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-166">Click OK.</span></span>
59. <span data-ttu-id="b6040-167">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="b6040-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="b6040-168">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="b6040-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="b6040-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b6040-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="b6040-170">Mapování prvků sestavy na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="b6040-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="b6040-171">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="b6040-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="b6040-172">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.</span><span class="sxs-lookup"><span data-stu-id="b6040-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b6040-173">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="b6040-174">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="b6040-175">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="b6040-176">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="b6040-177">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="b6040-178">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-178">Click Bind.</span></span>
9. <span data-ttu-id="b6040-179">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="b6040-180">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="b6040-181">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-181">Click Bind.</span></span>
12. <span data-ttu-id="b6040-182">Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="b6040-183">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="b6040-184">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-184">Click Bind.</span></span>
15. <span data-ttu-id="b6040-185">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="b6040-186">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="b6040-187">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-187">Click Bind.</span></span>
18. <span data-ttu-id="b6040-188">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="b6040-189">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="b6040-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="b6040-190">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-190">Click Bind.</span></span>
21. <span data-ttu-id="b6040-191">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="b6040-192">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="b6040-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="b6040-193">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-193">Click Bind.</span></span>
24. <span data-ttu-id="b6040-194">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="b6040-195">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="b6040-196">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-196">Click Bind.</span></span>
27. <span data-ttu-id="b6040-197">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="b6040-198">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="b6040-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="b6040-199">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-199">Click Bind.</span></span>
30. <span data-ttu-id="b6040-200">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="b6040-201">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="b6040-202">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-202">Click Bind.</span></span>
33. <span data-ttu-id="b6040-203">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="b6040-204">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="b6040-205">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-205">Click Bind.</span></span>
36. <span data-ttu-id="b6040-206">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="b6040-207">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="b6040-208">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-208">Click Bind.</span></span>
39. <span data-ttu-id="b6040-209">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="b6040-210">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="b6040-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="b6040-211">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-211">Click Bind.</span></span>
42. <span data-ttu-id="b6040-212">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="b6040-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="b6040-213">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="b6040-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="b6040-214">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="b6040-214">Click Bind.</span></span>
45. <span data-ttu-id="b6040-215">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b6040-215">Click Save.</span></span>
46. <span data-ttu-id="b6040-216">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b6040-216">Close the page.</span></span>

