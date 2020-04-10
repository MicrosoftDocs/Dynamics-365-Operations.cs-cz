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
ms.openlocfilehash: 7bbbc81eaf8c13e8d13e30a0276e38453e07ead9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142517"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="ee00f-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 3 - návrh sestavy)</span><span class="sxs-lookup"><span data-stu-id="ee00f-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee00f-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="ee00f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ee00f-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="ee00f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="ee00f-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").</span><span class="sxs-lookup"><span data-stu-id="ee00f-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="ee00f-107">Návrh sestavy k předložení finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="ee00f-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="ee00f-108">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="ee00f-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="ee00f-109">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="ee00f-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ee00f-110">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ee00f-111">V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".</span><span class="sxs-lookup"><span data-stu-id="ee00f-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="ee00f-112">Použijte model vytvořený předem jako zdroj dat pro novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="ee00f-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="ee00f-113">Do pole Název zadejte 'Sestava deníku hlavní knihy'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="ee00f-114">V poli Definice datového modelu vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="ee00f-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="ee00f-115">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="ee00f-115">Click Create configuration.</span></span>
8. <span data-ttu-id="ee00f-116">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="ee00f-116">Click Designer.</span></span>
9. <span data-ttu-id="ee00f-117">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="ee00f-118">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="ee00f-119">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="ee00f-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="ee00f-120">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-120">Click OK.</span></span>
13. <span data-ttu-id="ee00f-121">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="ee00f-122">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="ee00f-123">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="ee00f-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-124">Click OK.</span></span>
17. <span data-ttu-id="ee00f-125">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="ee00f-126">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="ee00f-127">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="ee00f-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="ee00f-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-128">Click OK.</span></span>
21. <span data-ttu-id="ee00f-129">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="ee00f-130">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ee00f-131">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="ee00f-132">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="ee00f-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="ee00f-133">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-133">Click OK.</span></span>
26. <span data-ttu-id="ee00f-134">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="ee00f-135">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="ee00f-136">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="ee00f-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="ee00f-137">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-137">Click OK.</span></span>
30. <span data-ttu-id="ee00f-138">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="ee00f-139">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="ee00f-140">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="ee00f-141">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="ee00f-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="ee00f-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-142">Click OK.</span></span>
35. <span data-ttu-id="ee00f-143">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="ee00f-144">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="ee00f-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="ee00f-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-145">Click OK.</span></span>
38. <span data-ttu-id="ee00f-146">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="ee00f-147">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="ee00f-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="ee00f-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-148">Click OK.</span></span>
41. <span data-ttu-id="ee00f-149">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="ee00f-150">Do pole Název zadejte 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="ee00f-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-151">Click OK.</span></span>
44. <span data-ttu-id="ee00f-152">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="ee00f-153">Do pole název zadejte 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="ee00f-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-154">Click OK.</span></span>
47. <span data-ttu-id="ee00f-155">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="ee00f-156">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="ee00f-157">Do pole Název dimenze zadejte Dimenze.</span><span class="sxs-lookup"><span data-stu-id="ee00f-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="ee00f-158">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-158">Click OK.</span></span>
51. <span data-ttu-id="ee00f-159">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="ee00f-160">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ee00f-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="ee00f-161">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="ee00f-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="ee00f-162">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="ee00f-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="ee00f-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-163">Click OK.</span></span>
56. <span data-ttu-id="ee00f-164">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="ee00f-165">Do pole Název zadejte Hodnota.</span><span class="sxs-lookup"><span data-stu-id="ee00f-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="ee00f-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-166">Click OK.</span></span>
59. <span data-ttu-id="ee00f-167">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="ee00f-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="ee00f-168">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="ee00f-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="ee00f-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee00f-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="ee00f-170">Mapování prvků sestavy na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="ee00f-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="ee00f-171">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="ee00f-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="ee00f-172">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="ee00f-173">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="ee00f-174">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="ee00f-175">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="ee00f-176">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="ee00f-177">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="ee00f-178">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-178">Click Bind.</span></span>
9. <span data-ttu-id="ee00f-179">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="ee00f-180">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="ee00f-181">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-181">Click Bind.</span></span>
12. <span data-ttu-id="ee00f-182">Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="ee00f-183">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="ee00f-184">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-184">Click Bind.</span></span>
15. <span data-ttu-id="ee00f-185">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="ee00f-186">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="ee00f-187">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-187">Click Bind.</span></span>
18. <span data-ttu-id="ee00f-188">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="ee00f-189">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="ee00f-190">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-190">Click Bind.</span></span>
21. <span data-ttu-id="ee00f-191">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="ee00f-192">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="ee00f-193">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-193">Click Bind.</span></span>
24. <span data-ttu-id="ee00f-194">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="ee00f-195">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="ee00f-196">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-196">Click Bind.</span></span>
27. <span data-ttu-id="ee00f-197">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="ee00f-198">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="ee00f-199">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-199">Click Bind.</span></span>
30. <span data-ttu-id="ee00f-200">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="ee00f-201">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="ee00f-202">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-202">Click Bind.</span></span>
33. <span data-ttu-id="ee00f-203">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="ee00f-204">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="ee00f-205">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-205">Click Bind.</span></span>
36. <span data-ttu-id="ee00f-206">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="ee00f-207">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="ee00f-208">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-208">Click Bind.</span></span>
39. <span data-ttu-id="ee00f-209">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="ee00f-210">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="ee00f-211">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-211">Click Bind.</span></span>
42. <span data-ttu-id="ee00f-212">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="ee00f-213">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="ee00f-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="ee00f-214">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="ee00f-214">Click Bind.</span></span>
45. <span data-ttu-id="ee00f-215">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ee00f-215">Click Save.</span></span>
46. <span data-ttu-id="ee00f-216">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ee00f-216">Close the page.</span></span>

