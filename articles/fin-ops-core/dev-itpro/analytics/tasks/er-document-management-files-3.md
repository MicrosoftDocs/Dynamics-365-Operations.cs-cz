---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 3 - Vytvoření formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví na použití souborů správy dokumentů ve výstupu ER. (část 3)
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
ms.openlocfilehash: 432cf4c41a7a223ab07b02edf6da7eac9965cff0
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092609"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a><span data-ttu-id="7ff61-104">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 3 - Vytvoření formátu)</span><span class="sxs-lookup"><span data-stu-id="7ff61-104">ER Use Document Management files in format outputs (Part 3 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7ff61-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7ff61-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="7ff61-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="7ff61-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="7ff61-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 2: Rozšíření datového modelu).</span><span class="sxs-lookup"><span data-stu-id="7ff61-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 2: Extend data model" procedure.</span></span>

<span data-ttu-id="7ff61-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="7ff61-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-to-process-invoices"></a><span data-ttu-id="7ff61-109">Vytvoření formátu pro zpracování faktur</span><span class="sxs-lookup"><span data-stu-id="7ff61-109">Create a format to process invoices</span></span>
1. <span data-ttu-id="7ff61-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7ff61-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7ff61-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="7ff61-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="7ff61-112">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="7ff61-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="7ff61-113">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="7ff61-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
    * <span data-ttu-id="7ff61-114">Vytvoříte formát pro generování elektronických zpráv s informacemi o všech souborech, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="7ff61-114">You will create a format to generate electronic messages with information about any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
5. <span data-ttu-id="7ff61-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="7ff61-116">V poli Nový zadejte Formát založený na datovém modelu Faktura odběratele (vlastní).</span><span class="sxs-lookup"><span data-stu-id="7ff61-116">In the New field, enter 'Format based on data model Customer invoice model (custom)'.</span></span>
7. <span data-ttu-id="7ff61-117">Do pole Název zadejte Vzorová zpráva elektronické faktury.</span><span class="sxs-lookup"><span data-stu-id="7ff61-117">In the Name field, type 'Electronic invoice sample message'.</span></span>
    * <span data-ttu-id="7ff61-118">Vzorová zpráva s elektronickou fakturou</span><span class="sxs-lookup"><span data-stu-id="7ff61-118">Electronic invoice sample message</span></span>  
8. <span data-ttu-id="7ff61-119">V poli Definice datového modelu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7ff61-119">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="7ff61-120">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="7ff61-120">InvoiceCustomer</span></span>  
9. <span data-ttu-id="7ff61-121">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="7ff61-121">Click Create configuration.</span></span>

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a><span data-ttu-id="7ff61-122">Návrh formátu k vyplnění příloh do generování zprávy ve formátu MIME</span><span class="sxs-lookup"><span data-stu-id="7ff61-122">Design a format to populate attachments into generating a message in MIME format</span></span>
1. <span data-ttu-id="7ff61-123">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="7ff61-123">Click Designer.</span></span>
2. <span data-ttu-id="7ff61-124">Klepnutím na možnost Přidat kořen otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-124">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="7ff61-125">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-125">In the tree, select 'XML\Element'.</span></span>
4. <span data-ttu-id="7ff61-126">Do pole Název zadejte Faktura.</span><span class="sxs-lookup"><span data-stu-id="7ff61-126">In the Name field, type 'Invoice'.</span></span>
    * <span data-ttu-id="7ff61-127">Faktura</span><span class="sxs-lookup"><span data-stu-id="7ff61-127">Invoice</span></span>  
5. <span data-ttu-id="7ff61-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-128">Click OK.</span></span>
6. <span data-ttu-id="7ff61-129">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-129">Click Add to open the drop dialog.</span></span>
7. <span data-ttu-id="7ff61-130">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-130">In the tree, select 'XML\Attribute'.</span></span>
8. <span data-ttu-id="7ff61-131">Do pole Název zadejte „SalesOrder“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-131">In the Name field, type 'SalesOrder'.</span></span>
    * <span data-ttu-id="7ff61-132">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="7ff61-132">SalesOrder</span></span>  
9. <span data-ttu-id="7ff61-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-133">Click OK.</span></span>
10. <span data-ttu-id="7ff61-134">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="7ff61-134">Click Add Attribute.</span></span>
11. <span data-ttu-id="7ff61-135">Do pole Název zadejte InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="7ff61-135">In the Name field, type 'InvoiceNumber'.</span></span>
    * <span data-ttu-id="7ff61-136">InvoiceNumber</span><span class="sxs-lookup"><span data-stu-id="7ff61-136">InvoiceNumber</span></span>  
12. <span data-ttu-id="7ff61-137">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-137">Click OK.</span></span>
13. <span data-ttu-id="7ff61-138">Klikněte na možnost Přidat atributy.</span><span class="sxs-lookup"><span data-stu-id="7ff61-138">Click Add Attribute.</span></span>
14. <span data-ttu-id="7ff61-139">Do pole Název zadejte InvoiceAmount.</span><span class="sxs-lookup"><span data-stu-id="7ff61-139">In the Name field, type 'InvoiceAmount'.</span></span>
    * <span data-ttu-id="7ff61-140">InvoiceAmount</span><span class="sxs-lookup"><span data-stu-id="7ff61-140">InvoiceAmount</span></span>  
15. <span data-ttu-id="7ff61-141">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-141">Click OK.</span></span>
16. <span data-ttu-id="7ff61-142">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-142">Click Add to open the drop dialog.</span></span>
17. <span data-ttu-id="7ff61-143">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-143">In the tree, select 'XML\Element'.</span></span>
18. <span data-ttu-id="7ff61-144">Do pole Název zadejte „EnclosedDocs“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-144">In the Name field, type 'EnclosedDocs'.</span></span>
    * <span data-ttu-id="7ff61-145">EnclosedDocs</span><span class="sxs-lookup"><span data-stu-id="7ff61-145">EnclosedDocs</span></span>  
19. <span data-ttu-id="7ff61-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-146">Click OK.</span></span>
20. <span data-ttu-id="7ff61-147">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs.</span><span class="sxs-lookup"><span data-stu-id="7ff61-147">In the tree, select 'Invoice\EnclosedDocs'.</span></span>
21. <span data-ttu-id="7ff61-148">Klepněte na Přidat prvek.</span><span class="sxs-lookup"><span data-stu-id="7ff61-148">Click Add Element.</span></span>
22. <span data-ttu-id="7ff61-149">Do pole Název zadejte Dokument.</span><span class="sxs-lookup"><span data-stu-id="7ff61-149">In the Name field, type 'Document'.</span></span>
    * <span data-ttu-id="7ff61-150">Doklad</span><span class="sxs-lookup"><span data-stu-id="7ff61-150">Document</span></span>  
23. <span data-ttu-id="7ff61-151">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-151">Click OK.</span></span>
24. <span data-ttu-id="7ff61-152">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.</span><span class="sxs-lookup"><span data-stu-id="7ff61-152">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
25. <span data-ttu-id="7ff61-153">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-153">Click Add to open the drop dialog.</span></span>
26. <span data-ttu-id="7ff61-154">Ve stromovém zobrazení vyberte „XML\Atribut“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-154">In the tree, select 'XML\Attribute'.</span></span>
27. <span data-ttu-id="7ff61-155">Do pole Název zadejte FileName.</span><span class="sxs-lookup"><span data-stu-id="7ff61-155">In the Name field, type 'FileName'.</span></span>
    * <span data-ttu-id="7ff61-156">Název souboru</span><span class="sxs-lookup"><span data-stu-id="7ff61-156">FileName</span></span>  
28. <span data-ttu-id="7ff61-157">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-157">Click OK.</span></span>
29. <span data-ttu-id="7ff61-158">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-158">Click Add to open the drop dialog.</span></span>
30. <span data-ttu-id="7ff61-159">Ve stromovém zobrazení vyberte „XML\Prvek“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-159">In the tree, select 'XML\Element'.</span></span>
31. <span data-ttu-id="7ff61-160">Do pole Název zadejte FileContent.</span><span class="sxs-lookup"><span data-stu-id="7ff61-160">In the Name field, type 'FileContent'.</span></span>
    * <span data-ttu-id="7ff61-161">FileContent</span><span class="sxs-lookup"><span data-stu-id="7ff61-161">FileContent</span></span>  
32. <span data-ttu-id="7ff61-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-162">Click OK.</span></span>
33. <span data-ttu-id="7ff61-163">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileContent.</span><span class="sxs-lookup"><span data-stu-id="7ff61-163">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent'.</span></span>
34. <span data-ttu-id="7ff61-164">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="7ff61-164">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="7ff61-165">Ve stromu vyberte 'Text\Base64'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-165">In the tree, select 'Text\Base64'.</span></span>
36. <span data-ttu-id="7ff61-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7ff61-166">Click OK.</span></span>

## <a name="map-format-elements-to-data-model-as-data-source"></a><span data-ttu-id="7ff61-167">Namapování prvků formátu na datový model jako zdroje dat</span><span class="sxs-lookup"><span data-stu-id="7ff61-167">Map format elements to data model as data source</span></span>
1. <span data-ttu-id="7ff61-168">Ve stromovém zobrazení vyberte možnost 'Faktura\SalesOrder'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-168">In the tree, select 'Invoice\SalesOrder'.</span></span>
2. <span data-ttu-id="7ff61-169">Klikněte na kartu Mapování.</span><span class="sxs-lookup"><span data-stu-id="7ff61-169">Click the Mapping tab.</span></span>
3. <span data-ttu-id="7ff61-170">Ve stromovém zobrazení rozbalte „model“.</span><span class="sxs-lookup"><span data-stu-id="7ff61-170">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="7ff61-171">Ve stromové struktuře vyberte 'model\Číslo prodejní objednávky(SalesId)'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-171">In the tree, select 'model\Sales order number(SalesId)'.</span></span>
5. <span data-ttu-id="7ff61-172">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-172">Click Bind.</span></span>
6. <span data-ttu-id="7ff61-173">Ve stromovém zobrazení vyberte možnost Faktura\InvoiceNumber.</span><span class="sxs-lookup"><span data-stu-id="7ff61-173">In the tree, select 'Invoice\InvoiceNumber'.</span></span>
7. <span data-ttu-id="7ff61-174">Ve stromovém zobrazení rozbalte možnost 'model\Základní faktura(InvoiceBase)'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-174">In the tree, expand 'model\Base invoice(InvoiceBase)'.</span></span>
8. <span data-ttu-id="7ff61-175">Ve stromové struktuře vyberte model\Základní faktura(InvoiceBase)\Číslo faktury(Id).</span><span class="sxs-lookup"><span data-stu-id="7ff61-175">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice number(Id)'.</span></span>
9. <span data-ttu-id="7ff61-176">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-176">Click Bind.</span></span>
10. <span data-ttu-id="7ff61-177">Ve stromovém zobrazení vyberte možnost 'Faktura\InvoiceAmount'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-177">In the tree, select 'Invoice\InvoiceAmount'.</span></span>
11. <span data-ttu-id="7ff61-178">Ve stromové struktuře vyberte 'model\Základní faktura(InvoiceBase)\Částka faktury(Amount)'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-178">In the tree, select 'model\Base invoice(InvoiceBase)\Invoice amount(Amount)'.</span></span>
12. <span data-ttu-id="7ff61-179">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-179">Click Bind.</span></span>
13. <span data-ttu-id="7ff61-180">Ve stromovém zobrazení rozbalte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-180">In the tree, expand 'model\Invoice attachments'.</span></span>
14. <span data-ttu-id="7ff61-181">Ve stromové struktuře vyberte model\Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="7ff61-181">In the tree, select 'model\Invoice attachments\File content'.</span></span>
15. <span data-ttu-id="7ff61-182">Ve stromovém zobrazení vyberte možnost 'Faktura\EnclosedDocs\Dokument\FileContent\Base64'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-182">In the tree, select 'Invoice\EnclosedDocs\Document\FileContent\Base64'.</span></span>
16. <span data-ttu-id="7ff61-183">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-183">Click Bind.</span></span>
17. <span data-ttu-id="7ff61-184">Ve stromovém zobrazení vyberte možnost 'modelPřílohy faktury\Název souboru'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-184">In the tree, select 'model\Invoice attachments\File name'.</span></span>
18. <span data-ttu-id="7ff61-185">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument\FileName.</span><span class="sxs-lookup"><span data-stu-id="7ff61-185">In the tree, select 'Invoice\EnclosedDocs\Document\FileName'.</span></span>
19. <span data-ttu-id="7ff61-186">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-186">Click Bind.</span></span>
20. <span data-ttu-id="7ff61-187">Ve stromovém zobrazení vyberte možnost 'model\Přílohy faktury'.</span><span class="sxs-lookup"><span data-stu-id="7ff61-187">In the tree, select 'model\Invoice attachments'.</span></span>
21. <span data-ttu-id="7ff61-188">Ve stromovém zobrazení vyberte možnost Faktura\EnclosedDocs\Dokument.</span><span class="sxs-lookup"><span data-stu-id="7ff61-188">In the tree, select 'Invoice\EnclosedDocs\Document'.</span></span>
22. <span data-ttu-id="7ff61-189">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="7ff61-189">Click Bind.</span></span>
23. <span data-ttu-id="7ff61-190">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7ff61-190">Click Save.</span></span>
24. <span data-ttu-id="7ff61-191">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7ff61-191">Close the page.</span></span>

