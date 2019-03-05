---
title: Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 29e19b6d91e5761178627ef2051f3385f5d7cfe5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/08/2019
ms.locfileid: "377542"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="82109-103">Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="82109-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82109-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="82109-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="82109-105">Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="82109-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="82109-106">V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu Mapování modelu na vybrané zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="82109-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="82109-107">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="82109-107">Create a new format configuration</span></span>
1. <span data-ttu-id="82109-108">Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="82109-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="82109-109">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="82109-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="82109-110">Ve stromovém zobrazení vyberte možnost **Platby (zjednodušený model)**.</span><span class="sxs-lookup"><span data-stu-id="82109-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="82109-111">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="82109-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="82109-112">Pokud se možnost **Vytvořit konfiguraci** nezobrazuje, musíte povolit režim návrhu na stránce **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="82109-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="82109-113">V poli **Nový** zadejte **Formát založený na datovém modelu PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="82109-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="82109-114">Do pole **Název** zadejte **BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="82109-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="82109-115">Do pole **Popis** zadejte **Formát plateb dodavatele BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="82109-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="82109-116">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="82109-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="82109-117">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="82109-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="82109-118">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="82109-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="82109-119">Lze definovat určitý formát elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="82109-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="82109-120">Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.</span><span class="sxs-lookup"><span data-stu-id="82109-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="82109-121">V poli **Definice datového modelu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="82109-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="82109-122">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="82109-122">Click **Create configuration**.</span></span> <span data-ttu-id="82109-123">Byla vytvořena nová konfigurace.</span><span class="sxs-lookup"><span data-stu-id="82109-123">A new configuration has been created.</span></span> <span data-ttu-id="82109-124">Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="82109-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="82109-125">Návrh formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="82109-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="82109-126">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="82109-126">Click **Designer**.</span></span>
2. <span data-ttu-id="82109-127">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="82109-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="82109-128">Ve stromovém zobrazení vyberte **Společné\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="82109-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="82109-129">Do pole **Název** zadejte **Xml**.</span><span class="sxs-lookup"><span data-stu-id="82109-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="82109-130">Zadejte hodnotu **UTF-8** do pole **Kódování**.</span><span class="sxs-lookup"><span data-stu-id="82109-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="82109-131">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-131">Click **OK**.</span></span>
7. <span data-ttu-id="82109-132">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="82109-132">Click **Add**.</span></span>
8. <span data-ttu-id="82109-133">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="82109-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="82109-134">Do pole **Název** zadejte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="82109-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="82109-135">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-135">Click **OK**.</span></span>
11. <span data-ttu-id="82109-136">Ve stromovém zobrazení vyberte **Xml\Message**.</span><span class="sxs-lookup"><span data-stu-id="82109-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="82109-137">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="82109-138">Do pole **Název** napište **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="82109-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="82109-139">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-139">Click **OK**.</span></span>
15. <span data-ttu-id="82109-140">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="82109-141">Do pole Název napište **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="82109-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="82109-142">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-142">Click **OK**.</span></span>
18. <span data-ttu-id="82109-143">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="82109-144">Do pole **Název** napište **Payments**.</span><span class="sxs-lookup"><span data-stu-id="82109-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="82109-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-145">Click **OK**.</span></span>
21. <span data-ttu-id="82109-146">Ve stromové struktuře vyberte **Xml\Message\Payments**.</span><span class="sxs-lookup"><span data-stu-id="82109-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="82109-147">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="82109-148">Do pole **Název** napište **Item**.</span><span class="sxs-lookup"><span data-stu-id="82109-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="82109-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-149">Click **OK**.</span></span>
25. <span data-ttu-id="82109-150">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="82109-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="82109-151">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="82109-151">Click **Add**.</span></span>
27. <span data-ttu-id="82109-152">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="82109-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="82109-153">Do pole Název zadejte **Id**.</span><span class="sxs-lookup"><span data-stu-id="82109-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="82109-154">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-154">Click **OK**.</span></span>
30. <span data-ttu-id="82109-155">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="82109-155">Click **Add**.</span></span>
31. <span data-ttu-id="82109-156">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="82109-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="82109-157">Do pole Název zadejte **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="82109-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="82109-158">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-158">Click **OK**.</span></span>
34. <span data-ttu-id="82109-159">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="82109-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="82109-160">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="82109-161">Do pole Název zadejte **Name**.</span><span class="sxs-lookup"><span data-stu-id="82109-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="82109-162">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-162">Click **OK**.</span></span>
38. <span data-ttu-id="82109-163">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="82109-164">Do pole **Název** zadejte **Bank**.</span><span class="sxs-lookup"><span data-stu-id="82109-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="82109-165">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-165">Click **OK**.</span></span>
41. <span data-ttu-id="82109-166">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank**.</span><span class="sxs-lookup"><span data-stu-id="82109-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="82109-167">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="82109-168">Do pole **Název** zadejte **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="82109-169">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-169">Click **OK**.</span></span>
45. <span data-ttu-id="82109-170">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="82109-171">Do pole **Název** zadejte **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="82109-172">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-172">Click **OK**.</span></span>
48. <span data-ttu-id="82109-173">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="82109-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="82109-174">Klepněte na tlačítko **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="82109-174">Click **Copy**.</span></span>
50. <span data-ttu-id="82109-175">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="82109-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="82109-176">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="82109-176">Click **Paste**.</span></span>
52. <span data-ttu-id="82109-177">Do pole **Název** zadejte **Payer**.</span><span class="sxs-lookup"><span data-stu-id="82109-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="82109-178">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="82109-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="82109-179">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="82109-180">Do pole **Název** zadejte **Currency**.</span><span class="sxs-lookup"><span data-stu-id="82109-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="82109-181">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-181">Click **OK**.</span></span>
57. <span data-ttu-id="82109-182">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="82109-183">Do pole **Název** zadejte **Description**.</span><span class="sxs-lookup"><span data-stu-id="82109-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="82109-184">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-184">Click **OK**.</span></span>
60. <span data-ttu-id="82109-185">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="82109-186">Do pole Název zadejte **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="82109-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="82109-187">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-187">Click **OK**.</span></span>
63. <span data-ttu-id="82109-188">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="82109-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="82109-189">Do pole Název zadejte **Amount**.</span><span class="sxs-lookup"><span data-stu-id="82109-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="82109-190">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="82109-191">Příprava součástí formátu pro mapování na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="82109-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="82109-192">Ve stromové struktuře vyberte **Xml\Message\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="82109-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="82109-193">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="82109-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="82109-194">Ve stromové struktuře vyberte **Text\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="82109-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="82109-195">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="82109-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="82109-196">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-196">Click **OK**.</span></span>
6. <span data-ttu-id="82109-197">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="82109-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="82109-198">Klikněte na možnost **Přidat DateTime**.</span><span class="sxs-lookup"><span data-stu-id="82109-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="82109-199">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="82109-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="82109-200">V poli **DateTime** vyberte **Date**.</span><span class="sxs-lookup"><span data-stu-id="82109-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="82109-201">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-201">Click **OK**.</span></span>
11. <span data-ttu-id="82109-202">Ve stromové struktuře vyberte **Xml\Message\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="82109-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="82109-203">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="82109-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="82109-204">Ve stromovém zobrazení vyberte **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="82109-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="82109-205">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-205">Click **OK**.</span></span>
15. <span data-ttu-id="82109-206">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Name**.</span><span class="sxs-lookup"><span data-stu-id="82109-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="82109-207">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-207">Click **Add String**.</span></span>
17. <span data-ttu-id="82109-208">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-208">Click **OK**.</span></span>
18. <span data-ttu-id="82109-209">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="82109-210">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-210">Click **Add String**.</span></span>
20. <span data-ttu-id="82109-211">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-211">Click **OK**.</span></span>
21. <span data-ttu-id="82109-212">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="82109-213">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-213">Click **Add String**.</span></span>
23. <span data-ttu-id="82109-214">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-214">Click **OK**.</span></span>
24. <span data-ttu-id="82109-215">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="82109-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="82109-216">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-216">Click **Add String**.</span></span>
26. <span data-ttu-id="82109-217">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-217">Click **OK**.</span></span>
27. <span data-ttu-id="82109-218">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="82109-219">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-219">Click **Add String**.</span></span>
29. <span data-ttu-id="82109-220">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-220">Click **OK**.</span></span>
30. <span data-ttu-id="82109-221">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="82109-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="82109-222">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-222">Click **Add String**.</span></span>
32. <span data-ttu-id="82109-223">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-223">Click **OK**.</span></span>
33. <span data-ttu-id="82109-224">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Currency**.</span><span class="sxs-lookup"><span data-stu-id="82109-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="82109-225">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-225">Click **Add String**.</span></span>
35. <span data-ttu-id="82109-226">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-226">Click **OK**.</span></span>
36. <span data-ttu-id="82109-227">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Description**.</span><span class="sxs-lookup"><span data-stu-id="82109-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="82109-228">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-228">Click **Add String**.</span></span>
38. <span data-ttu-id="82109-229">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-229">Click **OK**.</span></span>
39. <span data-ttu-id="82109-230">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Amount**.</span><span class="sxs-lookup"><span data-stu-id="82109-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="82109-231">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="82109-231">Click **Add String**.</span></span>
41. <span data-ttu-id="82109-232">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82109-232">Click **OK**.</span></span>
42. <span data-ttu-id="82109-233">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="82109-233">Click **Save**.</span></span>
43. <span data-ttu-id="82109-234">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="82109-234">Close the page.</span></span>

