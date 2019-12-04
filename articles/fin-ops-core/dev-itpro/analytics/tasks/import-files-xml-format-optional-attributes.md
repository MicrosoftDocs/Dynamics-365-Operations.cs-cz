---
title: (RCS) Import souborů v XML formátu s volitelnými atributy
description: Toto téma obsahuje informace o tom, jak může uživatel navrhnout konfiguraci formátu elektronického výkaznictví pro import souborů ve formátu XML, který obsahuje volitelné atributy.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34302a32b2e06f281dc93d6df160b88ffac7123
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769778"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="8e961-103">(RCS) Import souborů v XML formátu s volitelnými atributy</span><span class="sxs-lookup"><span data-stu-id="8e961-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8e961-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhovat konfiguraci elektronického výkaznictví pro import souborů v XML formátu obsahujícím volitelné atributy.</span><span class="sxs-lookup"><span data-stu-id="8e961-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="8e961-105">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="8e961-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="8e961-106">Než začnete, stáhněte a uložte místně soubor IncomingDocumentToLearnHowToHandleOptionalAttributes.xml z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="8e961-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="8e961-107">Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="8e961-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="8e961-108">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="8e961-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8e961-109">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8e961-109">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="8e961-110">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="8e961-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="8e961-111">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="8e961-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="8e961-112">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="8e961-113">V poli **Název** zadejte Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="8e961-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="8e961-114">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="8e961-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="8e961-115">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="8e961-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="8e961-116">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="8e961-117">Do pole **Název** zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="8e961-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="8e961-118">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8e961-118">Click **Add**.</span></span>
8.  <span data-ttu-id="8e961-119">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="8e961-120">Do pole **Název** zadejte Seznam.</span><span class="sxs-lookup"><span data-stu-id="8e961-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="8e961-121">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="8e961-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="8e961-122">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8e961-122">Click **Add**.</span></span>
12. <span data-ttu-id="8e961-123">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="8e961-124">Do pole **Název** zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="8e961-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="8e961-125">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="8e961-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="8e961-126">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8e961-126">Click **Add**.</span></span>
16. <span data-ttu-id="8e961-127">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-127">Click **Save**.</span></span>
17. <span data-ttu-id="8e961-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8e961-128">Close the page.</span></span>
18. <span data-ttu-id="8e961-129">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="8e961-129">Click **Change status**.</span></span>
19. <span data-ttu-id="8e961-130">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-130">Click **Complete**.</span></span>
20. <span data-ttu-id="8e961-131">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="8e961-132">Vytvoření formátu pro import dat</span><span class="sxs-lookup"><span data-stu-id="8e961-132">Create a format for data import</span></span>
1.  <span data-ttu-id="8e961-133">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="8e961-134">V poli **Nový** zadejte Formát založený na datovém modelu Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="8e961-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="8e961-135">V poli **Název** zadejte Formát pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="8e961-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="8e961-136">Vyberte možnost **Ano** v poli **Podporuje import dat**.</span><span class="sxs-lookup"><span data-stu-id="8e961-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="8e961-137">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="8e961-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="8e961-138">Návrh formátu pro analýzu příchozího souboru ve formátu XML</span><span class="sxs-lookup"><span data-stu-id="8e961-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="8e961-139">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="8e961-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="8e961-140">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8e961-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="8e961-141">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="8e961-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="8e961-142">Do pole **Název** zadejte kořen.</span><span class="sxs-lookup"><span data-stu-id="8e961-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="8e961-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-143">Click **OK**.</span></span>
6.  <span data-ttu-id="8e961-144">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="8e961-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="8e961-145">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="8e961-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="8e961-146">Do pole **Název** zadejte dokument.</span><span class="sxs-lookup"><span data-stu-id="8e961-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="8e961-147">V poli **Násobnost** vyberte **Jeden-n**.</span><span class="sxs-lookup"><span data-stu-id="8e961-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="8e961-148">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-148">Click **OK**.</span></span>
11. <span data-ttu-id="8e961-149">Ve stromovém zobrazení vyberte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="8e961-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="8e961-150">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="8e961-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="8e961-151">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="8e961-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="8e961-152">Do pole **Název** zadejte id.</span><span class="sxs-lookup"><span data-stu-id="8e961-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="8e961-153">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-153">Click **OK**.</span></span>
16. <span data-ttu-id="8e961-154">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="8e961-155">Návrh mapování formátu pro uložení analyzovaných informací do datového modelu</span><span class="sxs-lookup"><span data-stu-id="8e961-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="8e961-156">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="8e961-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="8e961-157">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="8e961-157">Click **New**.</span></span>
3. <span data-ttu-id="8e961-158">V poli **Definice** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8e961-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="8e961-159">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8e961-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="8e961-160">Do pole **Název** zadejte Mapování.</span><span class="sxs-lookup"><span data-stu-id="8e961-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="8e961-161">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-161">Click **Save**.</span></span>
7. <span data-ttu-id="8e961-162">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="8e961-162">Click **Designer**.</span></span>
8. <span data-ttu-id="8e961-163">Ve stromové struktuře rozbalte **formát**.</span><span class="sxs-lookup"><span data-stu-id="8e961-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="8e961-164">Ve stromovém zobrazení rozbalte **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="8e961-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="8e961-165">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8e961-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8e961-166">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="8e961-166">(document)\*\*.</span></span>
11. <span data-ttu-id="8e961-167">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="8e961-167">Click **Bind**.</span></span>
12. <span data-ttu-id="8e961-168">Ve stromovém zobrazení rozbalte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8e961-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8e961-169">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="8e961-169">(document)\*\*.</span></span>
13. <span data-ttu-id="8e961-170">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="8e961-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="8e961-171">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="8e961-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="8e961-172">Ve stromovém zobrazení rozbalte **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="8e961-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="8e961-173">Ve stromovém zobrazení zvolte **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="8e961-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="8e961-174">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="8e961-174">Click **Bind**.</span></span>
17. <span data-ttu-id="8e961-175">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-175">Click **Save**.</span></span>
18. <span data-ttu-id="8e961-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8e961-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="8e961-177">Spuštění mapování formátu</span><span class="sxs-lookup"><span data-stu-id="8e961-177">Run format mapping</span></span>
1. <span data-ttu-id="8e961-178">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-178">Click **Run**.</span></span>
2. <span data-ttu-id="8e961-179">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="8e961-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="8e961-180">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="8e961-181">Vybraný soubor nebyl naimportován, protože návrh formátu předpokládá existenci atributu ID pro prvek ‘document’, ale importovaný soubor neobsahuje žádný takový atribut.</span><span class="sxs-lookup"><span data-stu-id="8e961-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="8e961-182">Upravení struktury formátu pro zpracování atributu XML jako volitelného</span><span class="sxs-lookup"><span data-stu-id="8e961-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="8e961-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8e961-183">Close the page.</span></span>
2. <span data-ttu-id="8e961-184">Ve stromovém zobrazení rozbalte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="8e961-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="8e961-185">Ve stromovém zobrazení vyberte **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="8e961-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="8e961-186">V poli **Prázdný řetězec pro chybějící atribut** vyberte možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8e961-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="8e961-187">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="8e961-188">Spuštění mapování formátu pro testování změn</span><span class="sxs-lookup"><span data-stu-id="8e961-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="8e961-189">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="8e961-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="8e961-190">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="8e961-190">Click **Run**.</span></span>
3. <span data-ttu-id="8e961-191">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="8e961-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="8e961-192">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e961-192">Click **OK**.</span></span>
5. <span data-ttu-id="8e961-193">Prohlédněte si vygenerovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="8e961-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="8e961-194">Stejný soubor byl importován jako návrh formátu. V tomto okamžiku zvažte atribut ID pro prvek ‘document’ jako volitelný.</span><span class="sxs-lookup"><span data-stu-id="8e961-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>
