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
ms.openlocfilehash: fc28e9a2170929c6cd8daafd7eae54713cec36ff
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143193"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="74d1f-103">(RCS) Import souborů v XML formátu s volitelnými atributy</span><span class="sxs-lookup"><span data-stu-id="74d1f-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74d1f-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může navrhovat konfiguraci elektronického výkaznictví pro import souborů v XML formátu obsahujícím volitelné atributy.</span><span class="sxs-lookup"><span data-stu-id="74d1f-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="74d1f-105">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="74d1f-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="74d1f-106">Než začnete, stáhněte a uložte místně soubor IncomingDocumentToLearnHowToHandleOptionalAttributes.xml z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="74d1f-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="74d1f-107">Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="74d1f-108">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="74d1f-109">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="74d1f-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="74d1f-110">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="74d1f-111">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="74d1f-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="74d1f-112">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="74d1f-113">V poli **Název** zadejte Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="74d1f-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="74d1f-114">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="74d1f-115">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="74d1f-116">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="74d1f-117">Do pole **Název** zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="74d1f-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="74d1f-118">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-118">Click **Add**.</span></span>
8.    <span data-ttu-id="74d1f-119">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="74d1f-120">Do pole **Název** zadejte Seznam.</span><span class="sxs-lookup"><span data-stu-id="74d1f-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="74d1f-121">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="74d1f-122">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-122">Click **Add**.</span></span>
12.    <span data-ttu-id="74d1f-123">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="74d1f-124">Do pole **Název** zadejte Kód.</span><span class="sxs-lookup"><span data-stu-id="74d1f-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="74d1f-125">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="74d1f-126">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-126">Click **Add**.</span></span>
16.    <span data-ttu-id="74d1f-127">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-127">Click **Save**.</span></span>
17.    <span data-ttu-id="74d1f-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74d1f-128">Close the page.</span></span>
18.    <span data-ttu-id="74d1f-129">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="74d1f-130">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="74d1f-131">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="74d1f-132">Vytvoření formátu pro import dat</span><span class="sxs-lookup"><span data-stu-id="74d1f-132">Create a format for data import</span></span>
1.    <span data-ttu-id="74d1f-133">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="74d1f-134">V poli **Nový** zadejte Formát založený na datovém modelu Model pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="74d1f-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="74d1f-135">V poli **Název** zadejte Formát pro import souboru xml.</span><span class="sxs-lookup"><span data-stu-id="74d1f-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="74d1f-136">Vyberte možnost **Ano** v poli **Podporuje import dat**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="74d1f-137">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="74d1f-138">Návrh formátu pro analýzu příchozího souboru ve formátu XML</span><span class="sxs-lookup"><span data-stu-id="74d1f-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="74d1f-139">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="74d1f-140">Klepnutím na možnost **Přidat kořen** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="74d1f-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="74d1f-141">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="74d1f-142">Do pole **Název** zadejte kořen.</span><span class="sxs-lookup"><span data-stu-id="74d1f-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="74d1f-143">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-143">Click **OK**.</span></span>
6.    <span data-ttu-id="74d1f-144">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="74d1f-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="74d1f-145">Ve stromovém zobrazení vyberte **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="74d1f-146">Do pole **Název** zadejte dokument.</span><span class="sxs-lookup"><span data-stu-id="74d1f-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="74d1f-147">V poli **Násobnost** vyberte **Jeden-n**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="74d1f-148">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-148">Click **OK**.</span></span>
11.    <span data-ttu-id="74d1f-149">Ve stromovém zobrazení vyberte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="74d1f-150">Kliknutím na **Přidat** otevřete dialogové okno pro přetažení.</span><span class="sxs-lookup"><span data-stu-id="74d1f-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="74d1f-151">Ve stromovém zobrazení vyberte **XML\Attribute**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="74d1f-152">Do pole **Název** zadejte id.</span><span class="sxs-lookup"><span data-stu-id="74d1f-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="74d1f-153">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-153">Click **OK**.</span></span>
16.    <span data-ttu-id="74d1f-154">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="74d1f-155">Návrh mapování formátu pro uložení analyzovaných informací do datového modelu</span><span class="sxs-lookup"><span data-stu-id="74d1f-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="74d1f-156">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="74d1f-157">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-157">Click **New**.</span></span>
3. <span data-ttu-id="74d1f-158">V poli **Definice** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="74d1f-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="74d1f-159">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="74d1f-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="74d1f-160">Do pole **Název** zadejte Mapování.</span><span class="sxs-lookup"><span data-stu-id="74d1f-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="74d1f-161">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-161">Click **Save**.</span></span>
7. <span data-ttu-id="74d1f-162">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-162">Click **Designer**.</span></span>
8. <span data-ttu-id="74d1f-163">Ve stromové struktuře rozbalte **formát**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="74d1f-164">Ve stromovém zobrazení rozbalte **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="74d1f-165">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="74d1f-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="74d1f-166">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="74d1f-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="74d1f-167">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="74d1f-168">Ve stromovém zobrazení rozbalte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="74d1f-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="74d1f-169">(document)\*\*.</span><span class="sxs-lookup"><span data-stu-id="74d1f-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="74d1f-170">Ve stromovém zobrazení vyberte \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="74d1f-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="74d1f-171">(document)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="74d1f-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="74d1f-172">Ve stromovém zobrazení rozbalte **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="74d1f-173">Ve stromovém zobrazení zvolte **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="74d1f-174">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="74d1f-175">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-175">Click **Save**.</span></span>
18.    <span data-ttu-id="74d1f-176">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74d1f-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="74d1f-177">Spuštění mapování formátu</span><span class="sxs-lookup"><span data-stu-id="74d1f-177">Run format mapping</span></span>
1. <span data-ttu-id="74d1f-178">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-178">Click **Run**.</span></span>
2. <span data-ttu-id="74d1f-179">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="74d1f-180">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="74d1f-181">Vybraný soubor nebyl naimportován, protože návrh formátu předpokládá existenci atributu ID pro prvek ‘document’, ale importovaný soubor neobsahuje žádný takový atribut.</span><span class="sxs-lookup"><span data-stu-id="74d1f-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="74d1f-182">Upravení struktury formátu pro zpracování atributu XML jako volitelného</span><span class="sxs-lookup"><span data-stu-id="74d1f-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="74d1f-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="74d1f-183">Close the page.</span></span>
2. <span data-ttu-id="74d1f-184">Ve stromovém zobrazení rozbalte **root\document**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="74d1f-185">Ve stromovém zobrazení vyberte **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="74d1f-186">V poli **Prázdný řetězec pro chybějící atribut** vyberte možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="74d1f-187">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="74d1f-188">Spuštění mapování formátu pro testování změn</span><span class="sxs-lookup"><span data-stu-id="74d1f-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="74d1f-189">Klikněte na **Mapovat formát na model**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="74d1f-190">Klikněte na **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-190">Click **Run**.</span></span>
3. <span data-ttu-id="74d1f-191">Klikněte na **Procházet** a zvolte soubor **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="74d1f-192">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="74d1f-192">Click **OK**.</span></span>
5. <span data-ttu-id="74d1f-193">Prohlédněte si vygenerovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="74d1f-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="74d1f-194">Stejný soubor byl importován jako návrh formátu. V tomto okamžiku zvažte atribut ID pro prvek ‘document’ jako volitelný.</span><span class="sxs-lookup"><span data-stu-id="74d1f-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>
