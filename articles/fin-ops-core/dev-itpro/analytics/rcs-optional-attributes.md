---
title: Import souborů v XML formátu s volitelnými atributy
description: Toto téma obsahuje informace o navrhování formátů elektronického výkaznictví, které určují atributy XML pro analýzu příchozích elektronických dokumentů ve formátu XML.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182823"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="09d38-103">Import souborů v XML formátu s volitelnými atributy</span><span class="sxs-lookup"><span data-stu-id="09d38-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="09d38-104">Formáty elektronického výkaznictví můžete navrhovat pro analyzování příchozích dokumentů ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="09d38-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="09d38-105">Některé atributy prvků XML lze zadat v navrženém formátu elektronického výkaznictví jako volitelné.</span><span class="sxs-lookup"><span data-stu-id="09d38-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="09d38-106">To vám umožní zpracovat správně příchozí soubory s takovými atributy XML a bez nich.</span><span class="sxs-lookup"><span data-stu-id="09d38-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="09d38-107">Poté můžete obsah z těchto souborů použít k aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="09d38-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="09d38-108">Chcete-li získat další informace o této funkci, proveďte kroky v tématu [RCS Import souborů v XML formátu s volitelnými atributy](tasks/import-files-xml-format-optional-attributes.md), které je součástí obchodního procesu 7.5.4.3 Získání/vývoj součástí IT služeb/řešení (10677).</span><span class="sxs-lookup"><span data-stu-id="09d38-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="09d38-109">Tohoto průvodce záznamem úloh a přidružený vzorový soubor můžete stáhnout z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="09d38-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="09d38-110">Popis obsahu</span><span class="sxs-lookup"><span data-stu-id="09d38-110">Content description</span></span>       | <span data-ttu-id="09d38-111">Soubor</span><span class="sxs-lookup"><span data-stu-id="09d38-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="09d38-112">Vzorový soubor ve formátu XML</span><span class="sxs-lookup"><span data-stu-id="09d38-112">Sample file in XML format</span></span> | <span data-ttu-id="09d38-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="09d38-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="09d38-114">Průvodce úkolem</span><span class="sxs-lookup"><span data-stu-id="09d38-114">Task guide</span></span>                | <span data-ttu-id="09d38-115">RCS Import souborů v XML formátu s volitelnými atributy.axtr</span><span class="sxs-lookup"><span data-stu-id="09d38-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="09d38-116">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhovat konfiguraci elektronického výkaznictví pro import souborů v XML formátu obsahujícím volitelné atributy.</span><span class="sxs-lookup"><span data-stu-id="09d38-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="09d38-117">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="09d38-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="09d38-118">Než začnete, stáhněte a uložte místně soubor IncomingDocumentToLearnHowToHandleOptionalAttributes.xml z Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="09d38-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="09d38-119">Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="09d38-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="09d38-120">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="09d38-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="09d38-121">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="09d38-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="09d38-122">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="09d38-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="09d38-123">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="09d38-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="09d38-124">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="09d38-125">V poli **Název** zadejte Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="09d38-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="09d38-126">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="09d38-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="09d38-127">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="09d38-127">Click **Designer**.</span></span>
5. <span data-ttu-id="09d38-128">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="09d38-129">Do pole **Název** zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="09d38-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="09d38-130">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="09d38-130">Click **Add**.</span></span>
8. <span data-ttu-id="09d38-131">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="09d38-132">Do pole **Název** zadejte Seznam.</span><span class="sxs-lookup"><span data-stu-id="09d38-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="09d38-133">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="09d38-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="09d38-134">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="09d38-134">Click **Add**.</span></span>
12. <span data-ttu-id="09d38-135">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="09d38-136">Do pole **Název** zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="09d38-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="09d38-137">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="09d38-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="09d38-138">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="09d38-138">Click **Add**.</span></span>
16. <span data-ttu-id="09d38-139">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-139">Click **Save**.</span></span>
17. <span data-ttu-id="09d38-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="09d38-140">Close the page.</span></span>
18. <span data-ttu-id="09d38-141">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="09d38-141">Click **Change status**.</span></span>
19. <span data-ttu-id="09d38-142">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-142">Click **Complete**.</span></span>
20. <span data-ttu-id="09d38-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="09d38-144">Vytvoření formátu pro import dat</span><span class="sxs-lookup"><span data-stu-id="09d38-144">Create a format for data import</span></span>
1. <span data-ttu-id="09d38-145">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="09d38-146">V poli **Nový** zadejte Formát založený na datovém modelu Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="09d38-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="09d38-147">V poli **Název** zadejte Formát pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="09d38-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="09d38-148">Vyberte možnost **Ano** v poli **Podporuje import dat**.</span><span class="sxs-lookup"><span data-stu-id="09d38-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="09d38-149">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="09d38-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="09d38-150">Návrh formátu pro analýzu příchozího souboru ve formátu XML</span><span class="sxs-lookup"><span data-stu-id="09d38-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="09d38-151">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="09d38-151">Click **Designer**.</span></span>
2. <span data-ttu-id="09d38-152">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="09d38-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="09d38-153">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="09d38-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="09d38-154">Do pole **Název** zadejte kořen.</span><span class="sxs-lookup"><span data-stu-id="09d38-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="09d38-155">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-155">Click **OK**.</span></span>
6. <span data-ttu-id="09d38-156">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="09d38-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="09d38-157">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="09d38-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="09d38-158">Do pole **Název** zadejte dokument.</span><span class="sxs-lookup"><span data-stu-id="09d38-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="09d38-159">V poli **Násobnost** vyberte **Jeden-n**.</span><span class="sxs-lookup"><span data-stu-id="09d38-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="09d38-160">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-160">Click **OK**.</span></span>
11. <span data-ttu-id="09d38-161">Ve stromovém zobrazení vyberte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="09d38-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="09d38-162">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="09d38-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="09d38-163">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="09d38-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="09d38-164">Do pole **Název** zadejte id.</span><span class="sxs-lookup"><span data-stu-id="09d38-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="09d38-165">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-165">Click **OK**.</span></span>
16. <span data-ttu-id="09d38-166">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="09d38-167">Návrh mapování formátu pro uložení analyzovaných informací do datového modelu</span><span class="sxs-lookup"><span data-stu-id="09d38-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="09d38-168">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="09d38-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="09d38-169">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="09d38-169">Click **New**.</span></span>
3.  <span data-ttu-id="09d38-170">V poli **Definice** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="09d38-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="09d38-171">Do pole **Název** zadejte Mapování.</span><span class="sxs-lookup"><span data-stu-id="09d38-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="09d38-172">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-172">Click **Save**.</span></span>
6.  <span data-ttu-id="09d38-173">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="09d38-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="09d38-174">Ve stromové struktuře rozbalte **formát**.</span><span class="sxs-lookup"><span data-stu-id="09d38-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="09d38-175">Ve stromovém zobrazení rozbalte **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="09d38-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="09d38-176">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="09d38-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="09d38-177">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="09d38-177">(document)\*\*.</span></span>
10. <span data-ttu-id="09d38-178">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="09d38-178">Click **Bind**.</span></span>
11. <span data-ttu-id="09d38-179">Ve stromovém zobrazení rozbalte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="09d38-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="09d38-180">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="09d38-180">(document)\*\*.</span></span>
12. <span data-ttu-id="09d38-181">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="09d38-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="09d38-182">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="09d38-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="09d38-183">Ve stromovém zobrazení rozbalte **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="09d38-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="09d38-184">Ve stromovém zobrazení zvolte **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="09d38-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="09d38-185">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="09d38-185">Click **Bind**.</span></span>
16. <span data-ttu-id="09d38-186">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-186">Click **Save**.</span></span>
17. <span data-ttu-id="09d38-187">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="09d38-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="09d38-188">Spuštění mapování formátu</span><span class="sxs-lookup"><span data-stu-id="09d38-188">Run format mapping</span></span>
1. <span data-ttu-id="09d38-189">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-189">Click **Run**.</span></span>
2. <span data-ttu-id="09d38-190">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="09d38-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="09d38-191">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="09d38-192">Vybraný soubor nebyl naimportován, protože návrh formátu předpokládá existenci atributu ID pro prvek ‘document’, ale importovaný soubor neobsahuje žádný takový atribut.</span><span class="sxs-lookup"><span data-stu-id="09d38-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="09d38-193">Upravení struktury formátu pro zpracování atributu XML jako volitelného</span><span class="sxs-lookup"><span data-stu-id="09d38-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="09d38-194">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="09d38-194">Close the page.</span></span>
2. <span data-ttu-id="09d38-195">Ve stromovém zobrazení rozbalte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="09d38-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="09d38-196">Ve stromovém zobrazení vyberte **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="09d38-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="09d38-197">V poli **Prázdný řetězec pro chybějící atribut** vyberte možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="09d38-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="09d38-198">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="09d38-199">Spuštění mapování formátu pro testování změn</span><span class="sxs-lookup"><span data-stu-id="09d38-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="09d38-200">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="09d38-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="09d38-201">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="09d38-201">Click **Run**.</span></span>
3. <span data-ttu-id="09d38-202">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="09d38-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="09d38-203">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="09d38-203">Click **OK**.</span></span>
5. <span data-ttu-id="09d38-204">Prohlédněte si vygenerovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="09d38-204">Review the generated file.</span></span> <span data-ttu-id="09d38-205">Všimněte si, že stejný soubor byl importován jako návrh formátu. V tomto okamžiku zvažte atribut ID pro prvek ‘document’ jako volitelný.</span><span class="sxs-lookup"><span data-stu-id="09d38-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
