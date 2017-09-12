--- 
title: "Úprava a spuštění formátu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/31/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58e79f4d969e8bf0c7f150fd307f9f48334d6405
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="59c1b-103">Úprava a spuštění formátu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="59c1b-103">Modify and run format to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="59c1b-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="59c1b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="59c1b-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="59c1b-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="59c1b-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve formátu výstupy (část 4): spustit formát".</span><span class="sxs-lookup"><span data-stu-id="59c1b-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 4): Run format” procedure.</span></span>

<span data-ttu-id="59c1b-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="59c1b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="59c1b-108">Úprava formátu k vyplnění příloh do generování zpráv v binárním formátu</span><span class="sxs-lookup"><span data-stu-id="59c1b-108">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="59c1b-109">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="59c1b-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="59c1b-110">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="59c1b-110">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="59c1b-111">Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="59c1b-111">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="59c1b-112">Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".</span><span class="sxs-lookup"><span data-stu-id="59c1b-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="59c1b-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="59c1b-113">Click Designer.</span></span>
    * <span data-ttu-id="59c1b-114">Naplníte zprávu faktury v generování výstupu jako soubor XML s kódováním UNICODE.</span><span class="sxs-lookup"><span data-stu-id="59c1b-114">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="59c1b-115">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="59c1b-115">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="59c1b-116">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-116">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="59c1b-117">Do pole Název zadejte „Xml zpráva“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-117">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="59c1b-118">Zpráva Xml</span><span class="sxs-lookup"><span data-stu-id="59c1b-118">Xml message</span></span>  
9. <span data-ttu-id="59c1b-119">Zadejte hodnotu UTF-8 do pole Kódování.</span><span class="sxs-lookup"><span data-stu-id="59c1b-119">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="59c1b-120">UTF-8</span><span class="sxs-lookup"><span data-stu-id="59c1b-120">UTF-8</span></span>  
10. <span data-ttu-id="59c1b-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-121">Click OK.</span></span>
    * <span data-ttu-id="59c1b-122">Konfigurace generování výstupu jako souboru ZIP.</span><span class="sxs-lookup"><span data-stu-id="59c1b-122">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="59c1b-123">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="59c1b-123">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="59c1b-124">Ve stromovém zobrazení vyberte „Společné\Složka“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-124">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="59c1b-125">Do pole Název zadejte „Výstup Zip“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-125">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="59c1b-126">Výstup ZIP</span><span class="sxs-lookup"><span data-stu-id="59c1b-126">Zip output</span></span>  
14. <span data-ttu-id="59c1b-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-127">Click OK.</span></span>
15. <span data-ttu-id="59c1b-128">Ve stromu vyberte 'Výstup Zip'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-128">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="59c1b-129">Přidejte přílohy ke generujícímu souboru ZIP jako soubory s původními názvy a příponami.</span><span class="sxs-lookup"><span data-stu-id="59c1b-129">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="59c1b-130">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="59c1b-130">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="59c1b-131">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-131">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="59c1b-132">Do pole Název zadejte Připojený soubor.</span><span class="sxs-lookup"><span data-stu-id="59c1b-132">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="59c1b-133">Připojený soubor</span><span class="sxs-lookup"><span data-stu-id="59c1b-133">Attached file</span></span>  
19. <span data-ttu-id="59c1b-134">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-134">Click OK.</span></span>
20. <span data-ttu-id="59c1b-135">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-135">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="59c1b-136">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="59c1b-136">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="59c1b-137">Ve stromu vyberte 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-137">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="59c1b-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-138">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="59c1b-139">Mapování nových prvků formátu na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="59c1b-139">Map new format elements to data model</span></span>
1. <span data-ttu-id="59c1b-140">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="59c1b-140">Click the Mapping tab.</span></span>
2. <span data-ttu-id="59c1b-141">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-141">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="59c1b-142">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-142">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="59c1b-143">Ve stromu vyberte 'Výstup Zip\Připojený soubor\Base64'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-143">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="59c1b-144">Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="59c1b-144">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="59c1b-145">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="59c1b-145">Click Bind.</span></span>
7. <span data-ttu-id="59c1b-146">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-146">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="59c1b-147">Klikněte na Upravit název souboru.</span><span class="sxs-lookup"><span data-stu-id="59c1b-147">Click Edit filename.</span></span>
9. <span data-ttu-id="59c1b-148">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="59c1b-148">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="59c1b-149">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-149">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="59c1b-150">Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-150">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="59c1b-151">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="59c1b-151">Click Add data source.</span></span>
13. <span data-ttu-id="59c1b-152">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="59c1b-152">Click Save.</span></span>
14. <span data-ttu-id="59c1b-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59c1b-153">Close the page.</span></span>
15. <span data-ttu-id="59c1b-154">Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="59c1b-154">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="59c1b-155">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="59c1b-155">Click Bind.</span></span>
17. <span data-ttu-id="59c1b-156">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="59c1b-156">Click Save.</span></span>
18. <span data-ttu-id="59c1b-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="59c1b-157">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="59c1b-158">Spuštění sestavy navržené pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="59c1b-158">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="59c1b-159">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="59c1b-159">Click Run.</span></span>
2. <span data-ttu-id="59c1b-160">Rozbalte oddíl Záznamy k zahrnutí ().</span><span class="sxs-lookup"><span data-stu-id="59c1b-160">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="59c1b-161">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="59c1b-161">Click Filter.</span></span>
4. <span data-ttu-id="59c1b-162">Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="59c1b-162">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="59c1b-163">V poli Kritéria v poli Prodejní objednávka kritérií zadejte "Prodejní objednávka", zadejte číslo objednávky 000148.</span><span class="sxs-lookup"><span data-stu-id="59c1b-163">In the Criteria field, In the criteria “Sales order” field, type the order number 000148.</span></span>
    * <span data-ttu-id="59c1b-164">000148</span><span class="sxs-lookup"><span data-stu-id="59c1b-164">000148</span></span>  
6. <span data-ttu-id="59c1b-165">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-165">Click OK.</span></span>
7. <span data-ttu-id="59c1b-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="59c1b-166">Click OK.</span></span>
    * <span data-ttu-id="59c1b-167">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="59c1b-167">Review the generated output.</span></span> <span data-ttu-id="59c1b-168">Všimněte si, že kromě zprávy s fakturou zprávy ve formátu je pro každou přílohu vytvořen jeden soubor.</span><span class="sxs-lookup"><span data-stu-id="59c1b-168">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="59c1b-169">Soubory příloh jsou naplněny komprimovaným výstupem v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="59c1b-169">The attachment files are populated with the zipped output in binary format.</span></span>  


