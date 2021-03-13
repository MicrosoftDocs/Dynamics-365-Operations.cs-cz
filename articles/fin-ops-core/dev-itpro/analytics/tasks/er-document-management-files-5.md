---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 5)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f96189163d5ecac47ade9f713b3fd689e41352d0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092481"
---
# <a name="er-use-document-management-files-in-format-outputs-part-5---modify-and-run-format"></a><span data-ttu-id="9c829-104">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 5 - Změna a spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="9c829-104">ER Use Document Management files in format outputs (Part 5 - Modify and run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c829-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9c829-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9c829-106">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="9c829-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9c829-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve formátu výstupy (část 4: Spustit formát)".</span><span class="sxs-lookup"><span data-stu-id="9c829-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 4: Run format)" procedure.</span></span>

<span data-ttu-id="9c829-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="9c829-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a><span data-ttu-id="9c829-109">Úprava formátu k vyplnění příloh do generování zpráv v binárním formátu</span><span class="sxs-lookup"><span data-stu-id="9c829-109">Modify the format to populate attachments into generating messages in binary format</span></span>
1. <span data-ttu-id="9c829-110">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="9c829-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9c829-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="9c829-111">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="9c829-112">Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="9c829-112">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="9c829-113">Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".</span><span class="sxs-lookup"><span data-stu-id="9c829-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="9c829-114">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="9c829-114">Click Designer.</span></span>
    * <span data-ttu-id="9c829-115">Naplníte zprávu faktury v generování výstupu jako soubor XML s kódováním UNICODE.</span><span class="sxs-lookup"><span data-stu-id="9c829-115">You will populate the invoice message in the generating output as an XML file using UNICODE encoding.</span></span>  
6. <span data-ttu-id="9c829-116">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9c829-116">Click Add root to open the drop dialog.</span></span>
7. <span data-ttu-id="9c829-117">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="9c829-117">In the tree, select 'Common\File'.</span></span>
8. <span data-ttu-id="9c829-118">Do pole Název zadejte „Xml zpráva“.</span><span class="sxs-lookup"><span data-stu-id="9c829-118">In the Name field, type 'Xml message'.</span></span>
    * <span data-ttu-id="9c829-119">Zpráva Xml</span><span class="sxs-lookup"><span data-stu-id="9c829-119">Xml message</span></span>  
9. <span data-ttu-id="9c829-120">Zadejte hodnotu UTF-8 do pole Kódování.</span><span class="sxs-lookup"><span data-stu-id="9c829-120">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="9c829-121">UTF-8</span><span class="sxs-lookup"><span data-stu-id="9c829-121">UTF-8</span></span>  
10. <span data-ttu-id="9c829-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-122">Click OK.</span></span>
    * <span data-ttu-id="9c829-123">Konfigurace generování výstupu jako souboru ZIP.</span><span class="sxs-lookup"><span data-stu-id="9c829-123">Configure the generating output as a zipped file.</span></span>  
11. <span data-ttu-id="9c829-124">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9c829-124">Click Add root to open the drop dialog.</span></span>
12. <span data-ttu-id="9c829-125">Ve stromovém zobrazení vyberte „Společné\Složka“.</span><span class="sxs-lookup"><span data-stu-id="9c829-125">In the tree, select 'Common\Folder'.</span></span>
13. <span data-ttu-id="9c829-126">Do pole Název zadejte „Výstup Zip“.</span><span class="sxs-lookup"><span data-stu-id="9c829-126">In the Name field, type 'Zip output'.</span></span>
    * <span data-ttu-id="9c829-127">Výstup ZIP</span><span class="sxs-lookup"><span data-stu-id="9c829-127">Zip output</span></span>  
14. <span data-ttu-id="9c829-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-128">Click OK.</span></span>
15. <span data-ttu-id="9c829-129">Ve stromu vyberte 'Výstup Zip'.</span><span class="sxs-lookup"><span data-stu-id="9c829-129">In the tree, select 'Zip output'.</span></span>
    * <span data-ttu-id="9c829-130">Přidejte přílohy ke generujícímu souboru ZIP jako soubory s původními názvy a příponami.</span><span class="sxs-lookup"><span data-stu-id="9c829-130">Add attachments to the generating zipped file as files with original names and extensions.</span></span>  
16. <span data-ttu-id="9c829-131">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9c829-131">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="9c829-132">Ve stromovém zobrazení vyberte „Společné\Soubor“.</span><span class="sxs-lookup"><span data-stu-id="9c829-132">In the tree, select 'Common\File'.</span></span>
18. <span data-ttu-id="9c829-133">Do pole Název zadejte Připojený soubor.</span><span class="sxs-lookup"><span data-stu-id="9c829-133">In the Name field, type 'Attached file'.</span></span>
    * <span data-ttu-id="9c829-134">Připojený soubor</span><span class="sxs-lookup"><span data-stu-id="9c829-134">Attached file</span></span>  
19. <span data-ttu-id="9c829-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-135">Click OK.</span></span>
20. <span data-ttu-id="9c829-136">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="9c829-136">In the tree, select 'Zip output\Attached file'.</span></span>
21. <span data-ttu-id="9c829-137">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9c829-137">Click Add to open the drop dialog.</span></span>
22. <span data-ttu-id="9c829-138">Ve stromu vyberte 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9c829-138">In the tree, select 'Text\Base64'.</span></span>
23. <span data-ttu-id="9c829-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-139">Click OK.</span></span>

## <a name="map-new-format-elements-to-data-model"></a><span data-ttu-id="9c829-140">Mapování nových prvků formátu na prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="9c829-140">Map new format elements to data model</span></span>
1. <span data-ttu-id="9c829-141">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="9c829-141">Click the Mapping tab.</span></span>
2. <span data-ttu-id="9c829-142">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="9c829-142">In the tree, expand 'model'.</span></span>
3. <span data-ttu-id="9c829-143">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="9c829-143">In the tree, expand 'model\Invoice attachments'.</span></span>
4. <span data-ttu-id="9c829-144">Ve stromu vyberte 'Výstup Zip\Připojený soubor\Base64'.</span><span class="sxs-lookup"><span data-stu-id="9c829-144">In the tree, select 'Zip output\Attached file\Base64'.</span></span>
5. <span data-ttu-id="9c829-145">Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="9c829-145">In the tree, select 'model\Invoice attachments\File content'.</span></span>
6. <span data-ttu-id="9c829-146">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="9c829-146">Click Bind.</span></span>
7. <span data-ttu-id="9c829-147">Ve stromu vyberte 'Výstup Zip\Připojený soubor'.</span><span class="sxs-lookup"><span data-stu-id="9c829-147">In the tree, select 'Zip output\Attached file'.</span></span>
8. <span data-ttu-id="9c829-148">Klikněte na Upravit název souboru.</span><span class="sxs-lookup"><span data-stu-id="9c829-148">Click Edit filename.</span></span>
9. <span data-ttu-id="9c829-149">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="9c829-149">In the tree, expand 'model'.</span></span>
10. <span data-ttu-id="9c829-150">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="9c829-150">In the tree, expand 'model\Invoice attachments'.</span></span>
11. <span data-ttu-id="9c829-151">Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.</span><span class="sxs-lookup"><span data-stu-id="9c829-151">In the tree, select 'model\Invoice attachments\File name'.</span></span>
12. <span data-ttu-id="9c829-152">Klikněte na možnost Přidat datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="9c829-152">Click Add data source.</span></span>
13. <span data-ttu-id="9c829-153">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="9c829-153">Click Save.</span></span>
14. <span data-ttu-id="9c829-154">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9c829-154">Close the page.</span></span>
15. <span data-ttu-id="9c829-155">Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="9c829-155">In the tree, select 'model\Invoice attachments'.</span></span>
16. <span data-ttu-id="9c829-156">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="9c829-156">Click Bind.</span></span>
17. <span data-ttu-id="9c829-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9c829-157">Click Save.</span></span>
18. <span data-ttu-id="9c829-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9c829-158">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="9c829-159">Spuštění sestavy navržené pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="9c829-159">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="9c829-160">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="9c829-160">Click Run.</span></span>
2. <span data-ttu-id="9c829-161">Rozbalte oddíl Záznamy k zahrnutí ().</span><span class="sxs-lookup"><span data-stu-id="9c829-161">Expand the Records to include () section.</span></span>
3. <span data-ttu-id="9c829-162">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="9c829-162">Click Filter.</span></span>
4. <span data-ttu-id="9c829-163">Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="9c829-163">Select the row of the Customer invoice journal and the Sales order field.</span></span>
5. <span data-ttu-id="9c829-164">V poli Kritéria v poli Prodejní objednávka kritérií zadejte "Prodejní objednávka", zadejte číslo objednávky 000148.</span><span class="sxs-lookup"><span data-stu-id="9c829-164">In the Criteria field, In the criteria "Sales order" field, type the order number 000148.</span></span>
    * <span data-ttu-id="9c829-165">000148</span><span class="sxs-lookup"><span data-stu-id="9c829-165">000148</span></span>  
6. <span data-ttu-id="9c829-166">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-166">Click OK.</span></span>
7. <span data-ttu-id="9c829-167">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c829-167">Click OK.</span></span>
    * <span data-ttu-id="9c829-168">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="9c829-168">Review the generated output.</span></span> <span data-ttu-id="9c829-169">Všimněte si, že kromě zprávy s fakturou zprávy ve formátu je pro každou přílohu vytvořen jeden soubor.</span><span class="sxs-lookup"><span data-stu-id="9c829-169">Note,that in addition to the invoice message in XML format, a single file has been created for each attachment.</span></span> <span data-ttu-id="9c829-170">Soubory příloh jsou naplněny komprimovaným výstupem v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="9c829-170">The attachment files are populated with the zipped output in binary format.</span></span>  

