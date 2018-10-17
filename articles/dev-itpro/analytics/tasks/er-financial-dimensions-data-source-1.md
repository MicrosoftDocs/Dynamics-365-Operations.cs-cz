--- 
title: "Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1 - návrh datového modelu)"
description: "Následující postup popisuje, jak správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 84f546b73eefe3ead78c6ab3fdbbc05d0db5fef5
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="235d7-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1: návrh datového modelu)</span><span class="sxs-lookup"><span data-stu-id="235d7-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="235d7-104">Následující postup popisuje, jak správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="235d7-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="235d7-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="235d7-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="235d7-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="235d7-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="235d7-107">Vytvoření nového datového modelu</span><span class="sxs-lookup"><span data-stu-id="235d7-107">Create a new data model</span></span>
1. <span data-ttu-id="235d7-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="235d7-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="235d7-109">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="235d7-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="235d7-110">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="235d7-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="235d7-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="235d7-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="235d7-112">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="235d7-113">V poli Název zadejte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="235d7-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="235d7-114">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="235d7-114">Click Create configuration.</span></span>
6. <span data-ttu-id="235d7-115">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="235d7-115">Click Designer.</span></span>
7. <span data-ttu-id="235d7-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="235d7-117">Do pole Název zadejte Položka.</span><span class="sxs-lookup"><span data-stu-id="235d7-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="235d7-118">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-118">Click Add.</span></span>
10. <span data-ttu-id="235d7-119">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="235d7-120">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="235d7-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="235d7-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-121">Click Add.</span></span>
    * <span data-ttu-id="235d7-122">Přidáme do našeho modelu nový seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-122">We will add to our model a new record list.</span></span> <span data-ttu-id="235d7-123">Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) nastavení pro vybrané finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="235d7-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="235d7-124">Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími nastavení dimenze.</span><span class="sxs-lookup"><span data-stu-id="235d7-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="235d7-125">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="235d7-126">Do pole Název dimenze zadejte Nastavení dimenze.</span><span class="sxs-lookup"><span data-stu-id="235d7-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="235d7-127">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="235d7-128">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-128">Click Add.</span></span>
17. <span data-ttu-id="235d7-129">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="235d7-130">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="235d7-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="235d7-131">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="235d7-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="235d7-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-132">Click Add.</span></span>
21. <span data-ttu-id="235d7-133">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="235d7-134">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="235d7-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="235d7-135">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-135">Click Add.</span></span>
24. <span data-ttu-id="235d7-136">Ve stromovém zobrazení vyberte 'Položka'.</span><span class="sxs-lookup"><span data-stu-id="235d7-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="235d7-137">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="235d7-138">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="235d7-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="235d7-139">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="235d7-140">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-140">Click Add.</span></span>
29. <span data-ttu-id="235d7-141">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="235d7-142">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="235d7-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="235d7-143">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="235d7-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="235d7-144">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-144">Click Add.</span></span>
33. <span data-ttu-id="235d7-145">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="235d7-146">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="235d7-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="235d7-147">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="235d7-148">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-148">Click Add.</span></span>
37. <span data-ttu-id="235d7-149">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="235d7-150">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="235d7-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="235d7-151">V poli Typ položky vyberte Datum.</span><span class="sxs-lookup"><span data-stu-id="235d7-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="235d7-152">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-152">Click Add.</span></span>
41. <span data-ttu-id="235d7-153">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="235d7-154">Do pole Název zadejte Má dáti.</span><span class="sxs-lookup"><span data-stu-id="235d7-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="235d7-155">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="235d7-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="235d7-156">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-156">Click Add.</span></span>
45. <span data-ttu-id="235d7-157">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="235d7-158">Do pole Název zadejte Dal.</span><span class="sxs-lookup"><span data-stu-id="235d7-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="235d7-159">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-159">Click Add.</span></span>
48. <span data-ttu-id="235d7-160">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="235d7-161">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="235d7-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="235d7-162">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="235d7-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="235d7-163">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-163">Click Add.</span></span>
52. <span data-ttu-id="235d7-164">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="235d7-165">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="235d7-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="235d7-166">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-166">Click Add.</span></span>
55. <span data-ttu-id="235d7-167">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="235d7-168">Do pole Název zadejte Data dimenze.</span><span class="sxs-lookup"><span data-stu-id="235d7-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="235d7-169">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="235d7-170">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-170">Click Add.</span></span>
    * <span data-ttu-id="235d7-171">Přidali jsme do našeho modelu nový seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="235d7-171">We added to our model a new record list.</span></span> <span data-ttu-id="235d7-172">Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) hodnoty vybraných finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="235d7-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="235d7-173">Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="235d7-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="235d7-174">Název dimenze bude také prezentován v tomto záznamu jako pole, které se má v případě potřeby použít pro účely výběru.</span><span class="sxs-lookup"><span data-stu-id="235d7-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="235d7-175">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="235d7-176">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="235d7-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="235d7-177">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="235d7-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="235d7-178">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-178">Click Add.</span></span>
63. <span data-ttu-id="235d7-179">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="235d7-180">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="235d7-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="235d7-181">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-181">Click Add.</span></span>
66. <span data-ttu-id="235d7-182">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="235d7-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="235d7-183">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="235d7-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="235d7-184">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="235d7-184">Click Add.</span></span>
69. <span data-ttu-id="235d7-185">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="235d7-185">Click Save.</span></span>
70. <span data-ttu-id="235d7-186">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="235d7-186">Close the page.</span></span>


