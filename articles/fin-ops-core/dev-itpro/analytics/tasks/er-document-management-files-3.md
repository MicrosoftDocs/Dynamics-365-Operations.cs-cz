---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 3 - Vytvoření formátu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví k souborů správy dokumentů ve výstupu elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681846"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="47a3a-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 3 - Vytvoření formátu)</span><span class="sxs-lookup"><span data-stu-id="47a3a-103">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="47a3a-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="47a3a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="47a3a-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="47a3a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="47a3a-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 2: Rozšíření datového modelu).</span><span class="sxs-lookup"><span data-stu-id="47a3a-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="47a3a-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="47a3a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="47a3a-108">Vytvoření formátu pro zpracování faktur</span><span class="sxs-lookup"><span data-stu-id="47a3a-108">Create a format to process invoices</span></span>
1. <span data-ttu-id="47a3a-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="47a3a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="47a3a-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="47a3a-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="47a3a-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="47a3a-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="47a3a-112">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="47a3a-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="47a3a-113">Vytvoříte formát pro generování elektronických zpráv s informacemi o všech souborech, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="47a3a-113">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="47a3a-114">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-114">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="47a3a-115">V poli Nový zadejte Formát založený na datovém modelu Faktura odběratele (vlastní).</span><span class="sxs-lookup"><span data-stu-id="47a3a-115">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="47a3a-116">Do pole Název zadejte Vzorová zpráva elektronické faktury.</span><span class="sxs-lookup"><span data-stu-id="47a3a-116">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="47a3a-117">Vzorová zpráva s elektronickou fakturou</span><span class="sxs-lookup"><span data-stu-id="47a3a-117">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="47a3a-118">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="47a3a-118">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="47a3a-119">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="47a3a-119">InvoiceCustomer</span></span>  
9. <span data-ttu-id="47a3a-120">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="47a3a-120">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="47a3a-121">Návrh formátu k vyplnění příloh do generování zprávy ve formátu MIME</span><span class="sxs-lookup"><span data-stu-id="47a3a-121">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="47a3a-122">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="47a3a-122">Click Designer.</span></span>
2. <span data-ttu-id="47a3a-123">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-123">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="47a3a-124">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-124">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="47a3a-125">Do pole Název zadejte Faktura.</span><span class="sxs-lookup"><span data-stu-id="47a3a-125">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="47a3a-126">Faktura</span><span class="sxs-lookup"><span data-stu-id="47a3a-126">Invoice</span></span>  
5. <span data-ttu-id="47a3a-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-127">Click OK.</span></span>
6. <span data-ttu-id="47a3a-128">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-128">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="47a3a-129">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-129">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="47a3a-130">Do pole Název zadejte „SalesOrder“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-130">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="47a3a-131">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="47a3a-131">SalesOrder</span></span>  
9. <span data-ttu-id="47a3a-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-132">Click OK.</span></span>
10. <span data-ttu-id="47a3a-133">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="47a3a-133">Click Add Attribute.</span></span>
11. <span data-ttu-id="47a3a-134">Do pole Název zadejte InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="47a3a-134">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="47a3a-135">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="47a3a-135">InvoiceNumber</span></span>  
12. <span data-ttu-id="47a3a-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-136">Click OK.</span></span>
13. <span data-ttu-id="47a3a-137">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="47a3a-137">Click Add Attribute.</span></span>
14. <span data-ttu-id="47a3a-138">Do pole Název zadejte InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="47a3a-138">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="47a3a-139">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="47a3a-139">InvoiceAmount</span></span>  
15. <span data-ttu-id="47a3a-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-140">Click OK.</span></span>
16. <span data-ttu-id="47a3a-141">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-141">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="47a3a-142">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-142">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="47a3a-143">Do pole Název zadejte „EnclosedDocs“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-143">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="47a3a-144">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="47a3a-144">EnclosedDocs</span></span>  
19. <span data-ttu-id="47a3a-145">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-145">Click OK.</span></span>
20. <span data-ttu-id="47a3a-146">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="47a3a-146">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="47a3a-147">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="47a3a-147">Click Add Element.</span></span>
22. <span data-ttu-id="47a3a-148">Do pole Název zadejte Dokument.</span><span class="sxs-lookup"><span data-stu-id="47a3a-148">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="47a3a-149">Doklad</span><span class="sxs-lookup"><span data-stu-id="47a3a-149">Document</span></span>  
23. <span data-ttu-id="47a3a-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-150">Click OK.</span></span>
24. <span data-ttu-id="47a3a-151">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.</span><span class="sxs-lookup"><span data-stu-id="47a3a-151">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="47a3a-152">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-152">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="47a3a-153">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-153">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="47a3a-154">Do pole Název zadejte FileName.</span><span class="sxs-lookup"><span data-stu-id="47a3a-154">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="47a3a-155">Název souboru</span><span class="sxs-lookup"><span data-stu-id="47a3a-155">FileName</span></span>  
28. <span data-ttu-id="47a3a-156">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-156">Click OK.</span></span>
29. <span data-ttu-id="47a3a-157">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-157">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="47a3a-158">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-158">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="47a3a-159">Do pole Název zadejte FileContent.</span><span class="sxs-lookup"><span data-stu-id="47a3a-159">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="47a3a-160">FileContent</span><span class="sxs-lookup"><span data-stu-id="47a3a-160">FileContent</span></span>  
32. <span data-ttu-id="47a3a-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-161">Click OK.</span></span>
33. <span data-ttu-id="47a3a-162">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileContent.</span><span class="sxs-lookup"><span data-stu-id="47a3a-162">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="47a3a-163">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="47a3a-163">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="47a3a-164">Ve stromu vyberte 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-164">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="47a3a-165">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47a3a-165">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="47a3a-166">Namapování prvků formátu na datový model jako zdroje dat</span><span class="sxs-lookup"><span data-stu-id="47a3a-166">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="47a3a-167">Ve stromovém zobrazení vyberte možnost 'Faktura\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-167">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="47a3a-168">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="47a3a-168">Click the Mapping tab.</span></span>
3. <span data-ttu-id="47a3a-169">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="47a3a-169">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="47a3a-170">Ve stromové struktuře vyberte 'model\Číslo prodejní objednávky(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-170">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="47a3a-171">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-171">Click Bind.</span></span>
6. <span data-ttu-id="47a3a-172">Ve stromovém zobrazení vyberte možnost Faktura\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="47a3a-172">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="47a3a-173">Ve stromovém zobrazení rozbalte možnost 'model\Základní faktura(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-173">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="47a3a-174">Ve stromové struktuře vyberte model\Základní faktura(InvoiceBase)\Číslo faktury(Id).</span><span class="sxs-lookup"><span data-stu-id="47a3a-174">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="47a3a-175">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-175">Click Bind.</span></span>
10. <span data-ttu-id="47a3a-176">Ve stromovém zobrazení vyberte možnost 'Faktura\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-176">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="47a3a-177">Ve stromové struktuře vyberte 'model\Základní faktura(InvoiceBase)\Částka faktury(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-177">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="47a3a-178">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-178">Click Bind.</span></span>
13. <span data-ttu-id="47a3a-179">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-179">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="47a3a-180">Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="47a3a-180">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="47a3a-181">Ve stromovém zobrazení vyberte možnost 'Faktura\EnclosedDocs\Dokument\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-181">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="47a3a-182">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-182">Click Bind.</span></span>
17. <span data-ttu-id="47a3a-183">Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-183">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="47a3a-184">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileName.</span><span class="sxs-lookup"><span data-stu-id="47a3a-184">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="47a3a-185">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-185">Click Bind.</span></span>
20. <span data-ttu-id="47a3a-186">Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="47a3a-186">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="47a3a-187">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.</span><span class="sxs-lookup"><span data-stu-id="47a3a-187">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="47a3a-188">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="47a3a-188">Click Bind.</span></span>
23. <span data-ttu-id="47a3a-189">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="47a3a-189">Click Save.</span></span>
24. <span data-ttu-id="47a3a-190">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47a3a-190">Close the page.</span></span>

