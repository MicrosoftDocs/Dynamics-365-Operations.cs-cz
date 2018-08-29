--- 
title: "Návrh sestav k používání finančních dimenzí jako zdrojů dat"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="33138-103">Návrh sestav k používání finančních dimenzí jako zdrojů dat</span><span class="sxs-lookup"><span data-stu-id="33138-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33138-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="33138-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="33138-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="33138-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="33138-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 2: Mapování modelu").</span><span class="sxs-lookup"><span data-stu-id="33138-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="33138-107">Návrh sestavy k předložení finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="33138-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="33138-108">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="33138-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="33138-109">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="33138-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="33138-110">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="33138-111">V poli Nový zadejte "Formát založený na datovém modelu Vzorový datový model Finanční dimenze".</span><span class="sxs-lookup"><span data-stu-id="33138-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="33138-112">Použijte model vytvořený předem jako zdroj dat pro novou sestavu.</span><span class="sxs-lookup"><span data-stu-id="33138-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="33138-113">Do pole Název zadejte 'Sestava deníku hlavní knihy'.</span><span class="sxs-lookup"><span data-stu-id="33138-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="33138-114">V poli Definice datového modelu vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="33138-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="33138-115">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="33138-115">Click Create configuration.</span></span>
8. <span data-ttu-id="33138-116">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="33138-116">Click Designer.</span></span>
9. <span data-ttu-id="33138-117">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="33138-118">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="33138-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="33138-119">Do pole Název zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="33138-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="33138-120">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-120">Click OK.</span></span>
13. <span data-ttu-id="33138-121">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="33138-122">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="33138-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="33138-123">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="33138-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="33138-124">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-124">Click OK.</span></span>
17. <span data-ttu-id="33138-125">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="33138-126">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="33138-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="33138-127">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="33138-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="33138-128">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-128">Click OK.</span></span>
21. <span data-ttu-id="33138-129">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="33138-130">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="33138-131">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="33138-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="33138-132">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="33138-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="33138-133">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-133">Click OK.</span></span>
26. <span data-ttu-id="33138-134">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="33138-135">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="33138-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="33138-136">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="33138-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="33138-137">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-137">Click OK.</span></span>
30. <span data-ttu-id="33138-138">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="33138-139">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="33138-140">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="33138-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="33138-141">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="33138-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="33138-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-142">Click OK.</span></span>
35. <span data-ttu-id="33138-143">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="33138-144">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="33138-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="33138-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-145">Click OK.</span></span>
38. <span data-ttu-id="33138-146">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="33138-147">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="33138-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="33138-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-148">Click OK.</span></span>
41. <span data-ttu-id="33138-149">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="33138-150">Do pole Název zadejte 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="33138-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="33138-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-151">Click OK.</span></span>
44. <span data-ttu-id="33138-152">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="33138-153">Do pole název zadejte 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="33138-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="33138-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-154">Click OK.</span></span>
47. <span data-ttu-id="33138-155">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="33138-156">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="33138-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="33138-157">Do pole Název dimenze zadejte Dimenze.</span><span class="sxs-lookup"><span data-stu-id="33138-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="33138-158">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-158">Click OK.</span></span>
51. <span data-ttu-id="33138-159">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="33138-160">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33138-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="33138-161">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="33138-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="33138-162">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="33138-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="33138-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-163">Click OK.</span></span>
56. <span data-ttu-id="33138-164">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="33138-165">Do pole Název zadejte Hodnota.</span><span class="sxs-lookup"><span data-stu-id="33138-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="33138-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-166">Click OK.</span></span>
59. <span data-ttu-id="33138-167">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="33138-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="33138-168">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="33138-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="33138-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33138-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="33138-170">Mapování prvků sestavy na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="33138-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="33138-171">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="33138-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="33138-172">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze'.</span><span class="sxs-lookup"><span data-stu-id="33138-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="33138-173">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="33138-174">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="33138-175">Ve stromovém zobrazení rozbalte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="33138-176">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Popis: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="33138-177">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Popis: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="33138-178">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-178">Click Bind.</span></span>
9. <span data-ttu-id="33138-179">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML\Hodnota: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="33138-180">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Kód: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="33138-181">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-181">Click Bind.</span></span>
12. <span data-ttu-id="33138-182">Ve stromové struktuře vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Rozměry: Prvek XML\Kód: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="33138-183">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů\Název: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="33138-184">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-184">Click Bind.</span></span>
15. <span data-ttu-id="33138-185">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Data dimenzí: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="33138-186">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dimenze: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="33138-187">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-187">Click Bind.</span></span>
18. <span data-ttu-id="33138-188">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Ct: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="33138-189">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Dal: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="33138-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="33138-190">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-190">Click Bind.</span></span>
21. <span data-ttu-id="33138-191">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Dt: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="33138-192">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Má dáti: Skutečné'.</span><span class="sxs-lookup"><span data-stu-id="33138-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="33138-193">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-193">Click Bind.</span></span>
24. <span data-ttu-id="33138-194">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Měna: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="33138-195">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Měna: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="33138-196">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-196">Click Bind.</span></span>
27. <span data-ttu-id="33138-197">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Datum: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="33138-198">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Datum: Datum'.</span><span class="sxs-lookup"><span data-stu-id="33138-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="33138-199">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-199">Click Bind.</span></span>
30. <span data-ttu-id="33138-200">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML\Doklad: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="33138-201">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů\Doklad: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="33138-202">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-202">Click Bind.</span></span>
33. <span data-ttu-id="33138-203">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Transakce: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="33138-204">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Transakce: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="33138-205">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-205">Click Bind.</span></span>
36. <span data-ttu-id="33138-206">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML\Dávka: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="33138-207">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů\Dávka: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="33138-208">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-208">Click Bind.</span></span>
39. <span data-ttu-id="33138-209">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Deník: Prvek XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="33138-210">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Deník: Seznam záznamů'.</span><span class="sxs-lookup"><span data-stu-id="33138-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="33138-211">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-211">Click Bind.</span></span>
42. <span data-ttu-id="33138-212">Ve stromovém zobrazení vyberte 'Kořen: Prvek XML\Společnost: Atribut XML'.</span><span class="sxs-lookup"><span data-stu-id="33138-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="33138-213">Ve stromovém zobrazení vyberte 'model: Datový model: ukázkový model finanční dimenze\Společnost: Řetězec'.</span><span class="sxs-lookup"><span data-stu-id="33138-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="33138-214">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="33138-214">Click Bind.</span></span>
45. <span data-ttu-id="33138-215">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33138-215">Click Save.</span></span>
46. <span data-ttu-id="33138-216">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33138-216">Close the page.</span></span>


