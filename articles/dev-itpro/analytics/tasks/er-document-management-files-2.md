--- 
title: "Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2 - Rozšíření datového modelu)"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: cb4c58dc86a159a70634c05408a8db471ebcae4c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="b9a58-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2: Rozšíření datového modelu)</span><span class="sxs-lookup"><span data-stu-id="b9a58-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9a58-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b9a58-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="b9a58-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="b9a58-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b9a58-106">K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).</span><span class="sxs-lookup"><span data-stu-id="b9a58-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="b9a58-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="b9a58-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="b9a58-108">Rozšíření datového modelu na prezentaci souborů správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="b9a58-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="b9a58-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b9a58-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b9a58-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b9a58-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b9a58-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="b9a58-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="b9a58-112">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="b9a58-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="b9a58-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="b9a58-113">Click Designer.</span></span>
6. <span data-ttu-id="b9a58-114">Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="b9a58-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="b9a58-115">Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="b9a58-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="b9a58-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b9a58-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="b9a58-117">Do pole Název zadejte Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="b9a58-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="b9a58-118">Přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="b9a58-118">Invoice attachments</span></span>  
9. <span data-ttu-id="b9a58-119">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="b9a58-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="b9a58-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b9a58-120">Click Add.</span></span>
11. <span data-ttu-id="b9a58-121">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b9a58-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="b9a58-122">Do pole Název zadejte Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="b9a58-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="b9a58-123">Obsah souboru</span><span class="sxs-lookup"><span data-stu-id="b9a58-123">File content</span></span>  
13. <span data-ttu-id="b9a58-124">V poli Typ položky vyberte Obsahuje.</span><span class="sxs-lookup"><span data-stu-id="b9a58-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="b9a58-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b9a58-125">Click Add.</span></span>
15. <span data-ttu-id="b9a58-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b9a58-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="b9a58-127">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="b9a58-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="b9a58-128">Název souboru</span><span class="sxs-lookup"><span data-stu-id="b9a58-128">File name</span></span>  
17. <span data-ttu-id="b9a58-129">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="b9a58-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="b9a58-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b9a58-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a><span data-ttu-id="b9a58-131">Mapování nových prvků datového modelu do zdrojových dat aplikace Dynamics 365 for Finance and Operations, edice Enterprise</span><span class="sxs-lookup"><span data-stu-id="b9a58-131">Map new data model elements to Dynamics 365 for Finance and Operations, Enterprise edition data sources</span></span>
1. <span data-ttu-id="b9a58-132">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="b9a58-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="b9a58-133">Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="b9a58-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="b9a58-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="b9a58-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="b9a58-135">Namapujeme nové prvky modelu na příslušné zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="b9a58-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="b9a58-136">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="b9a58-136">Click Designer.</span></span>
4. <span data-ttu-id="b9a58-137">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="b9a58-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="b9a58-138">Ve stromovém zobrazení rozbalte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="b9a58-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="b9a58-139">Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.</span><span class="sxs-lookup"><span data-stu-id="b9a58-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="b9a58-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-140">Click Edit.</span></span>
8. <span data-ttu-id="b9a58-141">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="b9a58-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="b9a58-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="b9a58-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="b9a58-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-143">Click Save.</span></span>
10. <span data-ttu-id="b9a58-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-144">Close the page.</span></span>
11. <span data-ttu-id="b9a58-145">Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="b9a58-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="b9a58-146">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-146">Click Edit.</span></span>
13. <span data-ttu-id="b9a58-147">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="b9a58-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="b9a58-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="b9a58-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="b9a58-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-149">Click Save.</span></span>
15. <span data-ttu-id="b9a58-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-150">Close the page.</span></span>
16. <span data-ttu-id="b9a58-151">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="b9a58-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="b9a58-152">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-152">Click Edit.</span></span>
18. <span data-ttu-id="b9a58-153">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="b9a58-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="b9a58-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="b9a58-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="b9a58-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-155">Click Save.</span></span>
20. <span data-ttu-id="b9a58-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-156">Close the page.</span></span>
21. <span data-ttu-id="b9a58-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-157">Click Save.</span></span>
22. <span data-ttu-id="b9a58-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-158">Close the page.</span></span>
23. <span data-ttu-id="b9a58-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-159">Close the page.</span></span>
24. <span data-ttu-id="b9a58-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9a58-160">Close the page.</span></span>
25. <span data-ttu-id="b9a58-161">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="b9a58-161">Click Change status.</span></span>
26. <span data-ttu-id="b9a58-162">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="b9a58-162">Click Complete.</span></span>
27. <span data-ttu-id="b9a58-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b9a58-163">Click OK.</span></span>


