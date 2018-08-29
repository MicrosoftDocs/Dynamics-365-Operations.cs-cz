--- 
title: "Vytvoření konfigurací formátu elektronického výkaznictví"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="c390d-103">Vytvoření konfigurací formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="c390d-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c390d-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c390d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="c390d-105">Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="c390d-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="c390d-106">V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Mapování modelu na vybrané zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="c390d-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c390d-107">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="c390d-107">Create a new format configuration</span></span>
1. <span data-ttu-id="c390d-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c390d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="c390d-109">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c390d-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="c390d-110">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="c390d-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="c390d-111">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="c390d-112">V poli Nový zadejte "Formát založený na datovém modelu PaymentModel".</span><span class="sxs-lookup"><span data-stu-id="c390d-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="c390d-113">Do pole Název zadejte „BACS (Velká Británie – fiktivní)“.</span><span class="sxs-lookup"><span data-stu-id="c390d-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="c390d-114">BACS (Velká Británie – fiktivní)</span><span class="sxs-lookup"><span data-stu-id="c390d-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="c390d-115">Do pole Popis zadejte "Formát plateb dodavatele BACS (Velká Británie – fiktivní)".</span><span class="sxs-lookup"><span data-stu-id="c390d-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="c390d-116">Formát plateb dodavatele BACS (Velká Británie – fiktivní)</span><span class="sxs-lookup"><span data-stu-id="c390d-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="c390d-117">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="c390d-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c390d-118">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c390d-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c390d-119">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="c390d-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="c390d-120">Lze definovat určitý formát elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c390d-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="c390d-121">Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.</span><span class="sxs-lookup"><span data-stu-id="c390d-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="c390d-122">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="c390d-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="c390d-123">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c390d-123">Click Create configuration.</span></span>
    * <span data-ttu-id="c390d-124">Byla vytvořena nová konfigurace.</span><span class="sxs-lookup"><span data-stu-id="c390d-124">A new configuration has been created.</span></span> <span data-ttu-id="c390d-125">Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="c390d-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="c390d-126">Návrh formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="c390d-126">Design format of electronic document</span></span>
1. <span data-ttu-id="c390d-127">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c390d-127">Click Designer.</span></span>
2. <span data-ttu-id="c390d-128">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="c390d-129">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="c390d-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="c390d-130">Do pole Název zadejte „Xml“.</span><span class="sxs-lookup"><span data-stu-id="c390d-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="c390d-131">XML</span><span class="sxs-lookup"><span data-stu-id="c390d-131">Xml</span></span>  
5. <span data-ttu-id="c390d-132">Zadejte hodnotu UTF-8 do pole Kódování.</span><span class="sxs-lookup"><span data-stu-id="c390d-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="c390d-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="c390d-133">UTF-8</span></span>  
6. <span data-ttu-id="c390d-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-134">Click OK.</span></span>
7. <span data-ttu-id="c390d-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="c390d-136">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="c390d-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="c390d-137">Do pole Název zadejte „Zpráva“.</span><span class="sxs-lookup"><span data-stu-id="c390d-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="c390d-138">Zpráva</span><span class="sxs-lookup"><span data-stu-id="c390d-138">Message</span></span>  
10. <span data-ttu-id="c390d-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-139">Click OK.</span></span>
11. <span data-ttu-id="c390d-140">Ve stromovém zobrazení vyberte 'Xml\Zpráva'.</span><span class="sxs-lookup"><span data-stu-id="c390d-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="c390d-141">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-141">Click Add Element.</span></span>
13. <span data-ttu-id="c390d-142">Do pole Název zadejte „ProcessingDate“.</span><span class="sxs-lookup"><span data-stu-id="c390d-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="c390d-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="c390d-143">ProcessingDate</span></span>  
14. <span data-ttu-id="c390d-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-144">Click OK.</span></span>
15. <span data-ttu-id="c390d-145">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-145">Click Add Element.</span></span>
16. <span data-ttu-id="c390d-146">Do pole Název zadejte „MessageId“.</span><span class="sxs-lookup"><span data-stu-id="c390d-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="c390d-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="c390d-147">MessageId</span></span>  
17. <span data-ttu-id="c390d-148">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-148">Click OK.</span></span>
18. <span data-ttu-id="c390d-149">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-149">Click Add Element.</span></span>
19. <span data-ttu-id="c390d-150">Do pole Název zadejte Platby.</span><span class="sxs-lookup"><span data-stu-id="c390d-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c390d-151">Platby</span><span class="sxs-lookup"><span data-stu-id="c390d-151">Payments</span></span>  
20. <span data-ttu-id="c390d-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-152">Click OK.</span></span>
21. <span data-ttu-id="c390d-153">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby'.</span><span class="sxs-lookup"><span data-stu-id="c390d-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="c390d-154">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-154">Click Add Element.</span></span>
23. <span data-ttu-id="c390d-155">Do pole Název zadejte „Položka“.</span><span class="sxs-lookup"><span data-stu-id="c390d-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="c390d-156">Zboží</span><span class="sxs-lookup"><span data-stu-id="c390d-156">Item</span></span>  
24. <span data-ttu-id="c390d-157">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-157">Click OK.</span></span>
25. <span data-ttu-id="c390d-158">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.</span><span class="sxs-lookup"><span data-stu-id="c390d-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="c390d-159">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="c390d-160">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="c390d-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="c390d-161">Do pole Název zadejte „Id“.</span><span class="sxs-lookup"><span data-stu-id="c390d-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="c390d-162">ID</span><span class="sxs-lookup"><span data-stu-id="c390d-162">Id</span></span>  
29. <span data-ttu-id="c390d-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-163">Click OK.</span></span>
30. <span data-ttu-id="c390d-164">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="c390d-165">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="c390d-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="c390d-166">Do pole Název zadejte „Dodavatel“.</span><span class="sxs-lookup"><span data-stu-id="c390d-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="c390d-167">Dodavatel</span><span class="sxs-lookup"><span data-stu-id="c390d-167">Vendor</span></span>  
33. <span data-ttu-id="c390d-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-168">Click OK.</span></span>
34. <span data-ttu-id="c390d-169">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel'.</span><span class="sxs-lookup"><span data-stu-id="c390d-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="c390d-170">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-170">Click Add Element.</span></span>
36. <span data-ttu-id="c390d-171">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="c390d-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c390d-172">Jméno</span><span class="sxs-lookup"><span data-stu-id="c390d-172">Name</span></span>  
37. <span data-ttu-id="c390d-173">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-173">Click OK.</span></span>
38. <span data-ttu-id="c390d-174">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-174">Click Add Element.</span></span>
39. <span data-ttu-id="c390d-175">Do pole Název zadejte „Banka“.</span><span class="sxs-lookup"><span data-stu-id="c390d-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="c390d-176">Banka</span><span class="sxs-lookup"><span data-stu-id="c390d-176">Bank</span></span>  
40. <span data-ttu-id="c390d-177">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-177">Click OK.</span></span>
41. <span data-ttu-id="c390d-178">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.</span><span class="sxs-lookup"><span data-stu-id="c390d-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="c390d-179">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-179">Click Add Element.</span></span>
43. <span data-ttu-id="c390d-180">Do pole Název zadejte „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="c390d-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="c390d-181">Směrový kód</span><span class="sxs-lookup"><span data-stu-id="c390d-181">RoutingNumber</span></span>  
44. <span data-ttu-id="c390d-182">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-182">Click OK.</span></span>
45. <span data-ttu-id="c390d-183">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-183">Click Add Element.</span></span>
46. <span data-ttu-id="c390d-184">Do pole Název zadejte „AccountNumber“.</span><span class="sxs-lookup"><span data-stu-id="c390d-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="c390d-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="c390d-185">AccountNumber</span></span>  
47. <span data-ttu-id="c390d-186">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-186">Click OK.</span></span>
48. <span data-ttu-id="c390d-187">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel'.</span><span class="sxs-lookup"><span data-stu-id="c390d-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="c390d-188">Klepněte na tlačítko Kopírovat.</span><span class="sxs-lookup"><span data-stu-id="c390d-188">Click Copy.</span></span>
50. <span data-ttu-id="c390d-189">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.</span><span class="sxs-lookup"><span data-stu-id="c390d-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="c390d-190">Klepněte na tlačítko Vložit.</span><span class="sxs-lookup"><span data-stu-id="c390d-190">Click Paste.</span></span>
52. <span data-ttu-id="c390d-191">Do pole Název zadejte „Plátce“.</span><span class="sxs-lookup"><span data-stu-id="c390d-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="c390d-192">Plátce</span><span class="sxs-lookup"><span data-stu-id="c390d-192">Payer</span></span>  
53. <span data-ttu-id="c390d-193">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka'.</span><span class="sxs-lookup"><span data-stu-id="c390d-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="c390d-194">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-194">Click Add Element.</span></span>
55. <span data-ttu-id="c390d-195">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="c390d-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c390d-196">Měna</span><span class="sxs-lookup"><span data-stu-id="c390d-196">Currency</span></span>  
56. <span data-ttu-id="c390d-197">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-197">Click OK.</span></span>
57. <span data-ttu-id="c390d-198">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-198">Click Add Element.</span></span>
58. <span data-ttu-id="c390d-199">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="c390d-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="c390d-200">popis</span><span class="sxs-lookup"><span data-stu-id="c390d-200">Description</span></span>  
59. <span data-ttu-id="c390d-201">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-201">Click OK.</span></span>
60. <span data-ttu-id="c390d-202">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-202">Click Add Element.</span></span>
61. <span data-ttu-id="c390d-203">Do pole Název zadejte „TransDate“.</span><span class="sxs-lookup"><span data-stu-id="c390d-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="c390d-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="c390d-204">TransDate</span></span>  
62. <span data-ttu-id="c390d-205">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-205">Click OK.</span></span>
63. <span data-ttu-id="c390d-206">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="c390d-206">Click Add Element.</span></span>
64. <span data-ttu-id="c390d-207">Do pole Název zadejte „Částka“.</span><span class="sxs-lookup"><span data-stu-id="c390d-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="c390d-208">Množství</span><span class="sxs-lookup"><span data-stu-id="c390d-208">Amount</span></span>  
65. <span data-ttu-id="c390d-209">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="c390d-210">Příprava součástí formátu pro mapování na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="c390d-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="c390d-211">Ve stromové struktuře vyberte 'Xml\Zpráva\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="c390d-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="c390d-212">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="c390d-213">Ve stromové struktuře vyberte 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="c390d-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="c390d-214">V poli Formát zadejte „rrrr-MM-dd“.</span><span class="sxs-lookup"><span data-stu-id="c390d-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c390d-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c390d-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="c390d-216">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-216">Click OK.</span></span>
6. <span data-ttu-id="c390d-217">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="c390d-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="c390d-218">Klikněte na možnost Přidat datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c390d-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="c390d-219">V poli Formát zadejte „rrrr-MM-dd“.</span><span class="sxs-lookup"><span data-stu-id="c390d-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="c390d-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="c390d-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="c390d-221">V poli Typ data a času vyberte 'Datum'.</span><span class="sxs-lookup"><span data-stu-id="c390d-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="c390d-222">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-222">Click OK.</span></span>
11. <span data-ttu-id="c390d-223">Ve stromové struktuře vyberte 'Xml\Zpráva\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="c390d-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="c390d-224">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c390d-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="c390d-225">Ve stromovém zobrazení vyberte „Text\Řetězec“.</span><span class="sxs-lookup"><span data-stu-id="c390d-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="c390d-226">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-226">Click OK.</span></span>
15. <span data-ttu-id="c390d-227">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název'.</span><span class="sxs-lookup"><span data-stu-id="c390d-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="c390d-228">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-228">Click Add String.</span></span>
17. <span data-ttu-id="c390d-229">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-229">Click OK.</span></span>
18. <span data-ttu-id="c390d-230">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c390d-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="c390d-231">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-231">Click Add String.</span></span>
20. <span data-ttu-id="c390d-232">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-232">Click OK.</span></span>
21. <span data-ttu-id="c390d-233">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="c390d-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="c390d-234">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-234">Click Add String.</span></span>
23. <span data-ttu-id="c390d-235">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-235">Click OK.</span></span>
24. <span data-ttu-id="c390d-236">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Název'.</span><span class="sxs-lookup"><span data-stu-id="c390d-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="c390d-237">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-237">Click Add String.</span></span>
26. <span data-ttu-id="c390d-238">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-238">Click OK.</span></span>
27. <span data-ttu-id="c390d-239">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="c390d-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="c390d-240">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-240">Click Add String.</span></span>
29. <span data-ttu-id="c390d-241">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-241">Click OK.</span></span>
30. <span data-ttu-id="c390d-242">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Plátce\Banka\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="c390d-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="c390d-243">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-243">Click Add String.</span></span>
32. <span data-ttu-id="c390d-244">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-244">Click OK.</span></span>
33. <span data-ttu-id="c390d-245">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Měna'.</span><span class="sxs-lookup"><span data-stu-id="c390d-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="c390d-246">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-246">Click Add String.</span></span>
35. <span data-ttu-id="c390d-247">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-247">Click OK.</span></span>
36. <span data-ttu-id="c390d-248">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Popis'.</span><span class="sxs-lookup"><span data-stu-id="c390d-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="c390d-249">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-249">Click Add String.</span></span>
38. <span data-ttu-id="c390d-250">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-250">Click OK.</span></span>
39. <span data-ttu-id="c390d-251">Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Částka'.</span><span class="sxs-lookup"><span data-stu-id="c390d-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="c390d-252">Klepněte na tlačítko Přidat řetězec.</span><span class="sxs-lookup"><span data-stu-id="c390d-252">Click Add String.</span></span>
41. <span data-ttu-id="c390d-253">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c390d-253">Click OK.</span></span>
42. <span data-ttu-id="c390d-254">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c390d-254">Click Save.</span></span>
43. <span data-ttu-id="c390d-255">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c390d-255">Close the page.</span></span>


