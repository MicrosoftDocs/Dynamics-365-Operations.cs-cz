--- 
title: "Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="5b674-103">Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="5b674-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b674-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5b674-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="5b674-105">Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="5b674-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="5b674-106">V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Mapování modelu na vybrané zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="5b674-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="5b674-107">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="5b674-107">Create a new format configuration</span></span>
1. <span data-ttu-id="5b674-108">Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="5b674-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="5b674-109">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="5b674-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="5b674-110">Ve stromovém zobrazení vyberte možnost **Platby (zjednodušený model)**.</span><span class="sxs-lookup"><span data-stu-id="5b674-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="5b674-111">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5b674-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="5b674-112">Pokud se možnost **Vytvořit konfiguraci** nezobrazuje, musíte povolit režim návrhu na stránce **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="5b674-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="5b674-113">V poli **Nový** zadejte **Formát založený na datovém modelu PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="5b674-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="5b674-114">Do pole **Název** zadejte **BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="5b674-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="5b674-115">Do pole **Popis** zadejte **Formát plateb dodavatele BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="5b674-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="5b674-116">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="5b674-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="5b674-117">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="5b674-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="5b674-118">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="5b674-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="5b674-119">Lze definovat určitý formát elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5b674-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="5b674-120">Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.</span><span class="sxs-lookup"><span data-stu-id="5b674-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="5b674-121">V poli **Definice datového modelu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5b674-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="5b674-122">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="5b674-122">Click **Create configuration**.</span></span> <span data-ttu-id="5b674-123">Byla vytvořena nová konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5b674-123">A new configuration has been created.</span></span> <span data-ttu-id="5b674-124">Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="5b674-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="5b674-125">Pokud se možnost **Vytvořit konfiguraci** nezobrazuje, musíte povolit režim návrhu na stránce **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="5b674-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="5b674-126">Návrh formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="5b674-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="5b674-127">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="5b674-127">Click **Designer**.</span></span>
2. <span data-ttu-id="5b674-128">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5b674-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="5b674-129">Ve stromovém zobrazení vyberte **Společné\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="5b674-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="5b674-130">Do pole **Název** zadejte **Xml**.</span><span class="sxs-lookup"><span data-stu-id="5b674-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="5b674-131">Zadejte hodnotu **UTF-8** do pole **Kódování**.</span><span class="sxs-lookup"><span data-stu-id="5b674-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="5b674-132">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-132">Click **OK**.</span></span>
7. <span data-ttu-id="5b674-133">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5b674-133">Click **Add**.</span></span>
8. <span data-ttu-id="5b674-134">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="5b674-135">Do pole **Název** zadejte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="5b674-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="5b674-136">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-136">Click **OK**.</span></span>
11. <span data-ttu-id="5b674-137">Ve stromovém zobrazení vyberte **Xml\Message**.</span><span class="sxs-lookup"><span data-stu-id="5b674-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="5b674-138">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="5b674-139">Do pole **Název** napište **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="5b674-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="5b674-140">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-140">Click **OK**.</span></span>
15. <span data-ttu-id="5b674-141">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="5b674-142">Do pole Název napište **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="5b674-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="5b674-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-143">Click **OK**.</span></span>
18. <span data-ttu-id="5b674-144">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="5b674-145">Do pole **Název** napište **Payments**.</span><span class="sxs-lookup"><span data-stu-id="5b674-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="5b674-146">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-146">Click **OK**.</span></span>
21. <span data-ttu-id="5b674-147">Ve stromové struktuře vyberte **Xml\Message\Payments**.</span><span class="sxs-lookup"><span data-stu-id="5b674-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="5b674-148">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="5b674-149">Do pole **Název** napište **Item**.</span><span class="sxs-lookup"><span data-stu-id="5b674-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="5b674-150">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-150">Click **OK**.</span></span>
25. <span data-ttu-id="5b674-151">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="5b674-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="5b674-152">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5b674-152">Click **Add**.</span></span>
27. <span data-ttu-id="5b674-153">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="5b674-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="5b674-154">Do pole Název zadejte **Id**.</span><span class="sxs-lookup"><span data-stu-id="5b674-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="5b674-155">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-155">Click **OK**.</span></span>
30. <span data-ttu-id="5b674-156">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="5b674-156">Click **Add**.</span></span>
31. <span data-ttu-id="5b674-157">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="5b674-158">Do pole Název zadejte **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="5b674-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="5b674-159">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-159">Click **OK**.</span></span>
34. <span data-ttu-id="5b674-160">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="5b674-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="5b674-161">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="5b674-162">Do pole Název zadejte **Name**.</span><span class="sxs-lookup"><span data-stu-id="5b674-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="5b674-163">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-163">Click **OK**.</span></span>
38. <span data-ttu-id="5b674-164">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="5b674-165">Do pole **Název** zadejte **Bank**.</span><span class="sxs-lookup"><span data-stu-id="5b674-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="5b674-166">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-166">Click **OK**.</span></span>
41. <span data-ttu-id="5b674-167">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank**.</span><span class="sxs-lookup"><span data-stu-id="5b674-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="5b674-168">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="5b674-169">Do pole **Název** zadejte **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="5b674-170">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-170">Click **OK**.</span></span>
45. <span data-ttu-id="5b674-171">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="5b674-172">Do pole **Název** zadejte **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="5b674-173">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-173">Click **OK**.</span></span>
48. <span data-ttu-id="5b674-174">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="5b674-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="5b674-175">Klepněte na tlačítko **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="5b674-175">Click **Copy**.</span></span>
50. <span data-ttu-id="5b674-176">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="5b674-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="5b674-177">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="5b674-177">Click **Paste**.</span></span>
52. <span data-ttu-id="5b674-178">Do pole **Název** zadejte **Payer**.</span><span class="sxs-lookup"><span data-stu-id="5b674-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="5b674-179">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="5b674-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="5b674-180">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="5b674-181">Do pole **Název** zadejte **Currency**.</span><span class="sxs-lookup"><span data-stu-id="5b674-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="5b674-182">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-182">Click **OK**.</span></span>
57. <span data-ttu-id="5b674-183">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="5b674-184">Do pole **Název** zadejte **Description**.</span><span class="sxs-lookup"><span data-stu-id="5b674-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="5b674-185">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-185">Click **OK**.</span></span>
60. <span data-ttu-id="5b674-186">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="5b674-187">Do pole Název zadejte **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="5b674-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="5b674-188">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-188">Click **OK**.</span></span>
63. <span data-ttu-id="5b674-189">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="5b674-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="5b674-190">Do pole Název zadejte **Amount**.</span><span class="sxs-lookup"><span data-stu-id="5b674-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="5b674-191">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="5b674-192">Příprava součástí formátu pro mapování na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="5b674-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="5b674-193">Ve stromové struktuře vyberte **Xml\Message\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="5b674-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="5b674-194">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="5b674-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="5b674-195">Ve stromové struktuře vyberte **Text\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="5b674-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="5b674-196">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="5b674-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="5b674-197">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-197">Click **OK**.</span></span>
6. <span data-ttu-id="5b674-198">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="5b674-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="5b674-199">Klikněte na možnost **Přidat DateTime**.</span><span class="sxs-lookup"><span data-stu-id="5b674-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="5b674-200">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="5b674-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="5b674-201">V poli **DateTime** vyberte **Date**.</span><span class="sxs-lookup"><span data-stu-id="5b674-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="5b674-202">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-202">Click **OK**.</span></span>
11. <span data-ttu-id="5b674-203">Ve stromové struktuře vyberte **Xml\Message\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="5b674-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="5b674-204">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="5b674-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="5b674-205">Ve stromovém zobrazení vyberte **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="5b674-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="5b674-206">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-206">Click **OK**.</span></span>
15. <span data-ttu-id="5b674-207">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Name**.</span><span class="sxs-lookup"><span data-stu-id="5b674-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="5b674-208">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-208">Click **Add String**.</span></span>
17. <span data-ttu-id="5b674-209">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-209">Click **OK**.</span></span>
18. <span data-ttu-id="5b674-210">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="5b674-211">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-211">Click **Add String**.</span></span>
20. <span data-ttu-id="5b674-212">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-212">Click **OK**.</span></span>
21. <span data-ttu-id="5b674-213">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="5b674-214">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-214">Click **Add String**.</span></span>
23. <span data-ttu-id="5b674-215">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-215">Click **OK**.</span></span>
24. <span data-ttu-id="5b674-216">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="5b674-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="5b674-217">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-217">Click **Add String**.</span></span>
26. <span data-ttu-id="5b674-218">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-218">Click **OK**.</span></span>
27. <span data-ttu-id="5b674-219">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="5b674-220">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-220">Click **Add String**.</span></span>
29. <span data-ttu-id="5b674-221">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-221">Click **OK**.</span></span>
30. <span data-ttu-id="5b674-222">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="5b674-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="5b674-223">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-223">Click **Add String**.</span></span>
32. <span data-ttu-id="5b674-224">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-224">Click **OK**.</span></span>
33. <span data-ttu-id="5b674-225">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Currency**.</span><span class="sxs-lookup"><span data-stu-id="5b674-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="5b674-226">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-226">Click **Add String**.</span></span>
35. <span data-ttu-id="5b674-227">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-227">Click **OK**.</span></span>
36. <span data-ttu-id="5b674-228">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Description**.</span><span class="sxs-lookup"><span data-stu-id="5b674-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="5b674-229">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-229">Click **Add String**.</span></span>
38. <span data-ttu-id="5b674-230">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-230">Click **OK**.</span></span>
39. <span data-ttu-id="5b674-231">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Amount**.</span><span class="sxs-lookup"><span data-stu-id="5b674-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="5b674-232">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="5b674-232">Click **Add String**.</span></span>
41. <span data-ttu-id="5b674-233">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b674-233">Click **OK**.</span></span>
42. <span data-ttu-id="5b674-234">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="5b674-234">Click **Save**.</span></span>
43. <span data-ttu-id="5b674-235">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5b674-235">Close the page.</span></span>


