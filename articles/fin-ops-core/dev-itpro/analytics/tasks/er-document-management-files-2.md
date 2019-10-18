---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2 - Rozšíření datového modelu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 032f9c5707294ee33cc848ecc6990c1ef5bbfdbb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185030"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2-extend-data-model"></a><span data-ttu-id="dd750-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2: Rozšíření datového modelu)</span><span class="sxs-lookup"><span data-stu-id="dd750-103">ER Use Document Management files in format outputs (Part 2: Extend data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd750-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="dd750-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="dd750-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="dd750-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="dd750-106">K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).</span><span class="sxs-lookup"><span data-stu-id="dd750-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="dd750-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="dd750-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="dd750-108">Rozšíření datového modelu na prezentaci souborů správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="dd750-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="dd750-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="dd750-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="dd750-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="dd750-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="dd750-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="dd750-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="dd750-112">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="dd750-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="dd750-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="dd750-113">Click Designer.</span></span>
6. <span data-ttu-id="dd750-114">Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="dd750-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="dd750-115">Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="dd750-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="dd750-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="dd750-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="dd750-117">Do pole Název zadejte Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="dd750-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="dd750-118">Přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="dd750-118">Invoice attachments</span></span>  
9. <span data-ttu-id="dd750-119">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="dd750-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="dd750-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="dd750-120">Click Add.</span></span>
11. <span data-ttu-id="dd750-121">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="dd750-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="dd750-122">Do pole Název zadejte Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="dd750-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="dd750-123">Obsah souboru</span><span class="sxs-lookup"><span data-stu-id="dd750-123">File content</span></span>  
13. <span data-ttu-id="dd750-124">V poli Typ položky vyberte Obsahuje.</span><span class="sxs-lookup"><span data-stu-id="dd750-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="dd750-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="dd750-125">Click Add.</span></span>
15. <span data-ttu-id="dd750-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="dd750-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="dd750-127">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="dd750-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="dd750-128">Název souboru</span><span class="sxs-lookup"><span data-stu-id="dd750-128">File name</span></span>  
17. <span data-ttu-id="dd750-129">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="dd750-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="dd750-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="dd750-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="dd750-131">Namapování nových prvků datového modelu na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="dd750-131">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="dd750-132">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="dd750-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="dd750-133">Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="dd750-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="dd750-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="dd750-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="dd750-135">Namapujeme nové prvky modelu na příslušné zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="dd750-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="dd750-136">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="dd750-136">Click Designer.</span></span>
4. <span data-ttu-id="dd750-137">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="dd750-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="dd750-138">Ve stromovém zobrazení rozbalte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="dd750-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="dd750-139">Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.</span><span class="sxs-lookup"><span data-stu-id="dd750-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="dd750-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="dd750-140">Click Edit.</span></span>
8. <span data-ttu-id="dd750-141">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="dd750-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="dd750-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="dd750-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="dd750-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dd750-143">Click Save.</span></span>
10. <span data-ttu-id="dd750-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-144">Close the page.</span></span>
11. <span data-ttu-id="dd750-145">Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="dd750-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="dd750-146">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="dd750-146">Click Edit.</span></span>
13. <span data-ttu-id="dd750-147">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="dd750-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="dd750-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="dd750-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="dd750-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dd750-149">Click Save.</span></span>
15. <span data-ttu-id="dd750-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-150">Close the page.</span></span>
16. <span data-ttu-id="dd750-151">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="dd750-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="dd750-152">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="dd750-152">Click Edit.</span></span>
18. <span data-ttu-id="dd750-153">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="dd750-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="dd750-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="dd750-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="dd750-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dd750-155">Click Save.</span></span>
20. <span data-ttu-id="dd750-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-156">Close the page.</span></span>
21. <span data-ttu-id="dd750-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dd750-157">Click Save.</span></span>
22. <span data-ttu-id="dd750-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-158">Close the page.</span></span>
23. <span data-ttu-id="dd750-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-159">Close the page.</span></span>
24. <span data-ttu-id="dd750-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd750-160">Close the page.</span></span>
25. <span data-ttu-id="dd750-161">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="dd750-161">Click Change status.</span></span>
26. <span data-ttu-id="dd750-162">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="dd750-162">Click Complete.</span></span>
27. <span data-ttu-id="dd750-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dd750-163">Click OK.</span></span>

