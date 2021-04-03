---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1 - návrh datového modelu)
description: Toto téma popisuje, jak nakonfigurovat model elektronického výkaznictví (ER) tak, aby používal finanční dimenze jako zdroj dat pro zprávy ER. (část 1)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5ecae444d80698c03ac050b49894daa1b090f74
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570185"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="4099c-104">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 1 - návrh datového modelu)</span><span class="sxs-lookup"><span data-stu-id="4099c-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4099c-105">Následující postup popisuje, jak správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4099c-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="4099c-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="4099c-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="4099c-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="4099c-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="4099c-108">Vytvoření nového datového modelu</span><span class="sxs-lookup"><span data-stu-id="4099c-108">Create a new data model</span></span>
1. <span data-ttu-id="4099c-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4099c-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="4099c-110">Ujistěte se, že poskytovatel 'Litware, Inc.'</span><span class="sxs-lookup"><span data-stu-id="4099c-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="4099c-111">je k dispozici a označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="4099c-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="4099c-112">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="4099c-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="4099c-113">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="4099c-114">V poli Název zadejte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="4099c-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="4099c-115">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="4099c-115">Click Create configuration.</span></span>
6. <span data-ttu-id="4099c-116">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="4099c-116">Click Designer.</span></span>
7. <span data-ttu-id="4099c-117">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="4099c-118">Do pole Název zadejte Položka.</span><span class="sxs-lookup"><span data-stu-id="4099c-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="4099c-119">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-119">Click Add.</span></span>
10. <span data-ttu-id="4099c-120">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="4099c-121">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="4099c-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="4099c-122">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-122">Click Add.</span></span>
    * <span data-ttu-id="4099c-123">Přidáme do našeho modelu nový seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-123">We will add to our model a new record list.</span></span> <span data-ttu-id="4099c-124">Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) nastavení pro vybrané finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="4099c-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="4099c-125">Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími nastavení dimenze.</span><span class="sxs-lookup"><span data-stu-id="4099c-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="4099c-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="4099c-127">Do pole Název dimenze zadejte Nastavení dimenze.</span><span class="sxs-lookup"><span data-stu-id="4099c-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="4099c-128">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="4099c-129">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-129">Click Add.</span></span>
17. <span data-ttu-id="4099c-130">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="4099c-131">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="4099c-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="4099c-132">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="4099c-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="4099c-133">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-133">Click Add.</span></span>
21. <span data-ttu-id="4099c-134">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4099c-135">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="4099c-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="4099c-136">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-136">Click Add.</span></span>
24. <span data-ttu-id="4099c-137">Ve stromovém zobrazení vyberte 'Položka'.</span><span class="sxs-lookup"><span data-stu-id="4099c-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="4099c-138">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="4099c-139">Do pole Název zadejte Deník.</span><span class="sxs-lookup"><span data-stu-id="4099c-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="4099c-140">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="4099c-141">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-141">Click Add.</span></span>
29. <span data-ttu-id="4099c-142">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="4099c-143">Do pole Název zadejte Dávka.</span><span class="sxs-lookup"><span data-stu-id="4099c-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="4099c-144">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="4099c-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="4099c-145">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-145">Click Add.</span></span>
33. <span data-ttu-id="4099c-146">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="4099c-147">Do pole Název zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="4099c-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="4099c-148">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="4099c-149">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-149">Click Add.</span></span>
37. <span data-ttu-id="4099c-150">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="4099c-151">Do pole Název zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="4099c-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="4099c-152">V poli Typ položky vyberte Datum.</span><span class="sxs-lookup"><span data-stu-id="4099c-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="4099c-153">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-153">Click Add.</span></span>
41. <span data-ttu-id="4099c-154">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="4099c-155">Do pole Název zadejte Má dáti.</span><span class="sxs-lookup"><span data-stu-id="4099c-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="4099c-156">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="4099c-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="4099c-157">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-157">Click Add.</span></span>
45. <span data-ttu-id="4099c-158">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="4099c-159">Do pole Název zadejte Dal.</span><span class="sxs-lookup"><span data-stu-id="4099c-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="4099c-160">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-160">Click Add.</span></span>
48. <span data-ttu-id="4099c-161">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="4099c-162">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="4099c-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="4099c-163">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="4099c-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="4099c-164">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-164">Click Add.</span></span>
52. <span data-ttu-id="4099c-165">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="4099c-166">Do pole Název zadejte Doklad.</span><span class="sxs-lookup"><span data-stu-id="4099c-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="4099c-167">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-167">Click Add.</span></span>
55. <span data-ttu-id="4099c-168">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="4099c-169">Do pole Název zadejte Data dimenze.</span><span class="sxs-lookup"><span data-stu-id="4099c-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="4099c-170">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="4099c-171">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-171">Click Add.</span></span>
    * <span data-ttu-id="4099c-172">Přidali jsme do našeho modelu nový seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="4099c-172">We added to our model a new record list.</span></span> <span data-ttu-id="4099c-173">Tento seznam bude uvádět (pro všechny sestavy ER používající tento model jako zdroj dat) hodnoty vybraných finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="4099c-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="4099c-174">Každá finanční dimenze se zobrazí v tomto seznamu jako záznam s odpovídajícími poli představujícími hodnoty dimenze.</span><span class="sxs-lookup"><span data-stu-id="4099c-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="4099c-175">Název dimenze bude také prezentován v tomto záznamu jako pole, které se má v případě potřeby použít pro účely výběru.</span><span class="sxs-lookup"><span data-stu-id="4099c-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="4099c-176">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="4099c-177">Do pole Název zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="4099c-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="4099c-178">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="4099c-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="4099c-179">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-179">Click Add.</span></span>
63. <span data-ttu-id="4099c-180">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="4099c-181">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="4099c-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="4099c-182">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-182">Click Add.</span></span>
66. <span data-ttu-id="4099c-183">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="4099c-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="4099c-184">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="4099c-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="4099c-185">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4099c-185">Click Add.</span></span>
69. <span data-ttu-id="4099c-186">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="4099c-186">Click Save.</span></span>
70. <span data-ttu-id="4099c-187">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4099c-187">Close the page.</span></span>

![Stránka Návrhář modelu dat ER](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]