---
title: Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)
description: Toto téma vysvětluje, jak vytvořit konfiguraci formátu pro elektronické výkaznictví (ER).
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46686b9e4f6197f565a324a9d03cbb695b6a933b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749062"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="6e122-103">Elektronické vykazování – Vytvoření konfigurace formátu (listopad 2016)</span><span class="sxs-lookup"><span data-stu-id="6e122-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e122-104">Tohle téma popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit konfiguraci formátu pro elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6e122-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="6e122-105">Tato konfigurace formátu definuje formát elektronických dokumentů, které jsou použity pro zpracování plateb.</span><span class="sxs-lookup"><span data-stu-id="6e122-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="6e122-106">V tomto příkladu budete vytvářet konfiguraci formátu pro vzorovou společnost Litware, Inc. K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Mapování modelu na vybrané zdroje dat".</span><span class="sxs-lookup"><span data-stu-id="6e122-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="6e122-107">Vytvoření nové konfigurace formátu</span><span class="sxs-lookup"><span data-stu-id="6e122-107">Create a new format configuration</span></span>
1. <span data-ttu-id="6e122-108">Přejděte do části **Správa organizace > Pracovní prostory > Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="6e122-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="6e122-109">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="6e122-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="6e122-110">Ve stromovém zobrazení vyberte možnost **Platby (zjednodušený model)**.</span><span class="sxs-lookup"><span data-stu-id="6e122-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="6e122-111">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6e122-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="6e122-112">Pokud se možnost **Vytvořit konfiguraci** nezobrazuje, musíte povolit režim návrhu na stránce **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="6e122-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="6e122-113">V poli **Nový** zadejte **Formát založený na datovém modelu PaymentModel**.</span><span class="sxs-lookup"><span data-stu-id="6e122-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="6e122-114">Do pole **Název** zadejte **BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="6e122-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="6e122-115">Do pole **Popis** zadejte **Formát plateb dodavatele BACS (Velká Británie – fiktivní)**.</span><span class="sxs-lookup"><span data-stu-id="6e122-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="6e122-116">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="6e122-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="6e122-117">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6e122-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="6e122-118">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="6e122-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="6e122-119">Lze definovat určitý formát elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="6e122-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="6e122-120">Ponechejte toto pole prázdné, pokud chcete vybrat formát při spuštění.</span><span class="sxs-lookup"><span data-stu-id="6e122-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="6e122-121">V poli **Definice datového modelu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6e122-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="6e122-122">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="6e122-122">Click **Create configuration**.</span></span> <span data-ttu-id="6e122-123">Byla vytvořena nová konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6e122-123">A new configuration has been created.</span></span> <span data-ttu-id="6e122-124">Verzi konceptu lze použít k ukládání formát návrhu pro správu elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="6e122-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="6e122-125">Návrh formátu elektronického dokumentu</span><span class="sxs-lookup"><span data-stu-id="6e122-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="6e122-126">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="6e122-126">Click **Designer**.</span></span>
2. <span data-ttu-id="6e122-127">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6e122-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="6e122-128">Ve stromovém zobrazení vyberte **Společné\Soubor**.</span><span class="sxs-lookup"><span data-stu-id="6e122-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="6e122-129">Do pole **Název** zadejte **Xml**.</span><span class="sxs-lookup"><span data-stu-id="6e122-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="6e122-130">Zadejte hodnotu **UTF-8** do pole **Kódování**.</span><span class="sxs-lookup"><span data-stu-id="6e122-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="6e122-131">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-131">Click **OK**.</span></span>
7. <span data-ttu-id="6e122-132">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6e122-132">Click **Add**.</span></span>
8. <span data-ttu-id="6e122-133">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="6e122-134">Do pole **Název** zadejte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="6e122-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="6e122-135">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-135">Click **OK**.</span></span>
11. <span data-ttu-id="6e122-136">Ve stromovém zobrazení vyberte **Xml\Message**.</span><span class="sxs-lookup"><span data-stu-id="6e122-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="6e122-137">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="6e122-138">Do pole **Název** napište **ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6e122-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="6e122-139">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-139">Click **OK**.</span></span>
15. <span data-ttu-id="6e122-140">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="6e122-141">Do pole Název napište **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6e122-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="6e122-142">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-142">Click **OK**.</span></span>
18. <span data-ttu-id="6e122-143">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="6e122-144">Do pole **Název** napište **Payments**.</span><span class="sxs-lookup"><span data-stu-id="6e122-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="6e122-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-145">Click **OK**.</span></span>
21. <span data-ttu-id="6e122-146">Ve stromové struktuře vyberte **Xml\Message\Payments**.</span><span class="sxs-lookup"><span data-stu-id="6e122-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="6e122-147">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="6e122-148">Do pole **Název** napište **Item**.</span><span class="sxs-lookup"><span data-stu-id="6e122-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="6e122-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-149">Click **OK**.</span></span>
25. <span data-ttu-id="6e122-150">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="6e122-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="6e122-151">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6e122-151">Click **Add**.</span></span>
27. <span data-ttu-id="6e122-152">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="6e122-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="6e122-153">Do pole Název zadejte **Id**.</span><span class="sxs-lookup"><span data-stu-id="6e122-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="6e122-154">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-154">Click **OK**.</span></span>
30. <span data-ttu-id="6e122-155">Klikněte na položku **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="6e122-155">Click **Add**.</span></span>
31. <span data-ttu-id="6e122-156">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="6e122-157">Do pole Název zadejte **Vendor**.</span><span class="sxs-lookup"><span data-stu-id="6e122-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="6e122-158">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-158">Click **OK**.</span></span>
34. <span data-ttu-id="6e122-159">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="6e122-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="6e122-160">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="6e122-161">Do pole Název zadejte **Name**.</span><span class="sxs-lookup"><span data-stu-id="6e122-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="6e122-162">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-162">Click **OK**.</span></span>
38. <span data-ttu-id="6e122-163">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="6e122-164">Do pole **Název** zadejte **Bank**.</span><span class="sxs-lookup"><span data-stu-id="6e122-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="6e122-165">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-165">Click **OK**.</span></span>
41. <span data-ttu-id="6e122-166">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank**.</span><span class="sxs-lookup"><span data-stu-id="6e122-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="6e122-167">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="6e122-168">Do pole **Název** zadejte **RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="6e122-169">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-169">Click **OK**.</span></span>
45. <span data-ttu-id="6e122-170">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="6e122-171">Do pole **Název** zadejte **AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="6e122-172">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-172">Click **OK**.</span></span>
48. <span data-ttu-id="6e122-173">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor**.</span><span class="sxs-lookup"><span data-stu-id="6e122-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="6e122-174">Klepněte na tlačítko **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="6e122-174">Click **Copy**.</span></span>
50. <span data-ttu-id="6e122-175">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="6e122-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="6e122-176">Klepněte na tlačítko **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="6e122-176">Click **Paste**.</span></span>
52. <span data-ttu-id="6e122-177">Do pole **Název** zadejte **Payer**.</span><span class="sxs-lookup"><span data-stu-id="6e122-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="6e122-178">Ve stromové struktuře vyberte **Xml\Message\Payments\Item**.</span><span class="sxs-lookup"><span data-stu-id="6e122-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="6e122-179">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="6e122-180">Do pole **Název** zadejte **Currency**.</span><span class="sxs-lookup"><span data-stu-id="6e122-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="6e122-181">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-181">Click **OK**.</span></span>
57. <span data-ttu-id="6e122-182">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="6e122-183">Do pole **Název** zadejte **Description**.</span><span class="sxs-lookup"><span data-stu-id="6e122-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="6e122-184">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-184">Click **OK**.</span></span>
60. <span data-ttu-id="6e122-185">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="6e122-186">Do pole Název zadejte **TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6e122-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="6e122-187">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-187">Click **OK**.</span></span>
63. <span data-ttu-id="6e122-188">Klepněte na **Přidat element**.</span><span class="sxs-lookup"><span data-stu-id="6e122-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="6e122-189">Do pole Název zadejte **Amount**.</span><span class="sxs-lookup"><span data-stu-id="6e122-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="6e122-190">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="6e122-191">Příprava součástí formátu pro mapování na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="6e122-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="6e122-192">Ve stromové struktuře vyberte **Xml\Message\ProcessingDate**.</span><span class="sxs-lookup"><span data-stu-id="6e122-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="6e122-193">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="6e122-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="6e122-194">Ve stromové struktuře vyberte **Text\DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6e122-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="6e122-195">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6e122-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="6e122-196">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-196">Click **OK**.</span></span>
6. <span data-ttu-id="6e122-197">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="6e122-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="6e122-198">Klikněte na možnost **Přidat DateTime**.</span><span class="sxs-lookup"><span data-stu-id="6e122-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="6e122-199">Do pole **Formát** zadejte **yyyy-MM-dd**.</span><span class="sxs-lookup"><span data-stu-id="6e122-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="6e122-200">V poli **DateTime** vyberte **Date**.</span><span class="sxs-lookup"><span data-stu-id="6e122-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="6e122-201">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-201">Click **OK**.</span></span>
11. <span data-ttu-id="6e122-202">Ve stromové struktuře vyberte **Xml\Message\MessageId**.</span><span class="sxs-lookup"><span data-stu-id="6e122-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="6e122-203">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="6e122-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="6e122-204">Ve stromovém zobrazení vyberte **Text\String**.</span><span class="sxs-lookup"><span data-stu-id="6e122-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="6e122-205">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-205">Click **OK**.</span></span>
15. <span data-ttu-id="6e122-206">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Name**.</span><span class="sxs-lookup"><span data-stu-id="6e122-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="6e122-207">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-207">Click **Add String**.</span></span>
17. <span data-ttu-id="6e122-208">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-208">Click **OK**.</span></span>
18. <span data-ttu-id="6e122-209">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="6e122-210">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-210">Click **Add String**.</span></span>
20. <span data-ttu-id="6e122-211">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-211">Click **OK**.</span></span>
21. <span data-ttu-id="6e122-212">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="6e122-213">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-213">Click **Add String**.</span></span>
23. <span data-ttu-id="6e122-214">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-214">Click **OK**.</span></span>
24. <span data-ttu-id="6e122-215">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Name**.</span><span class="sxs-lookup"><span data-stu-id="6e122-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="6e122-216">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-216">Click **Add String**.</span></span>
26. <span data-ttu-id="6e122-217">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-217">Click **OK**.</span></span>
27. <span data-ttu-id="6e122-218">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="6e122-219">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-219">Click **Add String**.</span></span>
29. <span data-ttu-id="6e122-220">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-220">Click **OK**.</span></span>
30. <span data-ttu-id="6e122-221">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="6e122-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="6e122-222">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-222">Click **Add String**.</span></span>
32. <span data-ttu-id="6e122-223">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-223">Click **OK**.</span></span>
33. <span data-ttu-id="6e122-224">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Currency**.</span><span class="sxs-lookup"><span data-stu-id="6e122-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="6e122-225">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-225">Click **Add String**.</span></span>
35. <span data-ttu-id="6e122-226">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-226">Click **OK**.</span></span>
36. <span data-ttu-id="6e122-227">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Description**.</span><span class="sxs-lookup"><span data-stu-id="6e122-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="6e122-228">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-228">Click **Add String**.</span></span>
38. <span data-ttu-id="6e122-229">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-229">Click **OK**.</span></span>
39. <span data-ttu-id="6e122-230">Ve stromové struktuře vyberte **Xml\Message\Payments\Item\Amount**.</span><span class="sxs-lookup"><span data-stu-id="6e122-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="6e122-231">Klikněte na **Přidat řetězec**.</span><span class="sxs-lookup"><span data-stu-id="6e122-231">Click **Add String**.</span></span>
41. <span data-ttu-id="6e122-232">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e122-232">Click **OK**.</span></span>
42. <span data-ttu-id="6e122-233">Klikněte na tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6e122-233">Click **Save**.</span></span>
43. <span data-ttu-id="6e122-234">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6e122-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]