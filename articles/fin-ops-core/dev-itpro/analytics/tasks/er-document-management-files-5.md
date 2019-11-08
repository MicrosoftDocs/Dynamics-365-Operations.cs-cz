---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERComponentTypeDropDialog, ERExpressionDesignerFormula, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: de075899547d194fb9eb0e68947efd005c101851
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550687"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="70c12-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="70c12-103">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70c12-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="70c12-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="70c12-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="70c12-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="70c12-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve formátu výstupy (část 4: Spustit formát)".</span><span class="sxs-lookup"><span data-stu-id="70c12-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4: Run format)” procedure.</span></span>

<span data-ttu-id="70c12-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="70c12-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="70c12-108">Úprava formátu k vyplnění příloh do generování zpráv v binárním formátu</span><span class="sxs-lookup"><span data-stu-id="70c12-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="70c12-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="70c12-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="70c12-110">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="70c12-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="70c12-111">Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="70c12-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="70c12-112">Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".</span><span class="sxs-lookup"><span data-stu-id="70c12-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="70c12-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="70c12-113">Click Designer.</span></span>
    * <span data-ttu-id="70c12-114">Naplníte zprávu faktury v generování výstupu jako soubor XML s kódováním UNICODE.</span><span class="sxs-lookup"><span data-stu-id="70c12-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="70c12-115">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="70c12-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="70c12-116">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="70c12-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="70c12-117">Do pole Název zadejte „Xml zpráva“.</span><span class="sxs-lookup"><span data-stu-id="70c12-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="70c12-118">Zpráva Xml</span><span class="sxs-lookup"><span data-stu-id="70c12-118">Xml message</span></span>  
9. <span data-ttu-id="70c12-119">Zadejte hodnotu UTF-8 do pole Kódování.</span><span class="sxs-lookup"><span data-stu-id="70c12-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="70c12-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="70c12-120">UTF-8</span></span>  
10. <span data-ttu-id="70c12-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-121">Click OK.</span></span>
    * <span data-ttu-id="70c12-122">Konfigurace generování výstupu jako souboru ZIP.</span><span class="sxs-lookup"><span data-stu-id="70c12-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="70c12-123">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="70c12-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="70c12-124">Ve stromovém zobrazení vyberte „Společné\Složka“.</span><span class="sxs-lookup"><span data-stu-id="70c12-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="70c12-125">Do pole Název zadejte „Výstup Zip“.</span><span class="sxs-lookup"><span data-stu-id="70c12-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="70c12-126">Výstup ZIP</span><span class="sxs-lookup"><span data-stu-id="70c12-126">Zip output</span></span>  
14. <span data-ttu-id="70c12-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-127">Click OK.</span></span>
15. <span data-ttu-id="70c12-128">Ve stromu vyberte 'Výstup Zip'.</span><span class="sxs-lookup"><span data-stu-id="70c12-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="70c12-129">Přidejte přílohy ke generujícímu souboru ZIP jako soubory s původními názvy a příponami.</span><span class="sxs-lookup"><span data-stu-id="70c12-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="70c12-130">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="70c12-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="70c12-131">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="70c12-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="70c12-132">Do pole Název zadejte Připojený soubor.</span><span class="sxs-lookup"><span data-stu-id="70c12-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="70c12-133">Připojený soubor</span><span class="sxs-lookup"><span data-stu-id="70c12-133">Attached file</span></span>  
19. <span data-ttu-id="70c12-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-134">Click OK.</span></span>
20. <span data-ttu-id="70c12-135">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="70c12-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="70c12-136">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="70c12-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="70c12-137">Ve stromu vyberte 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="70c12-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="70c12-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="70c12-139">Mapování nových prvků formátu na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="70c12-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="70c12-140">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="70c12-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="70c12-141">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="70c12-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="70c12-142">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="70c12-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="70c12-143">Ve stromu vyberte 'Výstup Zip\Připojený soubor\Base64'.</span><span class="sxs-lookup"><span data-stu-id="70c12-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="70c12-144">Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="70c12-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="70c12-145">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="70c12-145">Click Bind.</span></span>
7. <span data-ttu-id="70c12-146">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="70c12-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="70c12-147">Klikněte na Upravit název souboru.</span><span class="sxs-lookup"><span data-stu-id="70c12-147">Click Edit filename.</span></span>
9. <span data-ttu-id="70c12-148">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="70c12-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="70c12-149">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="70c12-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="70c12-150">Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.</span><span class="sxs-lookup"><span data-stu-id="70c12-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="70c12-151">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="70c12-151">Click Add data source.</span></span>
13. <span data-ttu-id="70c12-152">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="70c12-152">Click Save.</span></span>
14. <span data-ttu-id="70c12-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="70c12-153">Close the page.</span></span>
15. <span data-ttu-id="70c12-154">Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="70c12-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="70c12-155">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="70c12-155">Click Bind.</span></span>
17. <span data-ttu-id="70c12-156">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="70c12-156">Click Save.</span></span>
18. <span data-ttu-id="70c12-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="70c12-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="70c12-158">Spuštění sestavy navržené pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="70c12-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="70c12-159">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="70c12-159">Click Run.</span></span>
2. <span data-ttu-id="70c12-160">Rozbalte oddíl Záznamy k zahrnutí ().</span><span class="sxs-lookup"><span data-stu-id="70c12-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="70c12-161">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="70c12-161">Click Filter.</span></span>
4. <span data-ttu-id="70c12-162">Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="70c12-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="70c12-163">V poli Kritéria v poli Prodejní objednávka kritérií zadejte "Prodejní objednávka", zadejte číslo objednávky 000148.</span><span class="sxs-lookup"><span data-stu-id="70c12-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="70c12-164">000148</span><span class="sxs-lookup"><span data-stu-id="70c12-164">000148</span></span>  
6. <span data-ttu-id="70c12-165">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-165">Click OK.</span></span>
7. <span data-ttu-id="70c12-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="70c12-166">Click OK.</span></span>
    * <span data-ttu-id="70c12-167">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="70c12-167">Review the generated output.</span></span> <span data-ttu-id="70c12-168">Všimněte si, že kromě zprávy s fakturou zprávy ve formátu je pro každou přílohu vytvořen jeden soubor.</span><span class="sxs-lookup"><span data-stu-id="70c12-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="70c12-169">Soubory příloh jsou naplněny komprimovaným výstupem v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="70c12-169">The attachment files are populated with the zipped output in binary format.</span></span>  

