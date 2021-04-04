---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2 - Rozšíření datového modelu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví (ER) na použití souborů (příloh) správy dokumentů ve výstupu ER. (část 2)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b47c35790ce04a494b6c58f6e04fa9b829d2ab93
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559766"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a><span data-ttu-id="5dd2f-104">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 2 - Rozšíření datového modelu)</span><span class="sxs-lookup"><span data-stu-id="5dd2f-104">ER Use Document Management files in format outputs (Part 2 - Extend data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5dd2f-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-105">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="5dd2f-106">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="5dd2f-107">K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).</span><span class="sxs-lookup"><span data-stu-id="5dd2f-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 1: Prepare data model)" task guide.</span></span>

<span data-ttu-id="5dd2f-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="5dd2f-109">Rozšíření datového modelu na prezentaci souborů správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="5dd2f-109">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="5dd2f-110">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5dd2f-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="5dd2f-112">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-112">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="5dd2f-113">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="5dd2f-113">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="5dd2f-114">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-114">Click Designer.</span></span>
6. <span data-ttu-id="5dd2f-115">Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="5dd2f-115">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="5dd2f-116">Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-116">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="5dd2f-117">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="5dd2f-118">Do pole Název zadejte Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-118">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="5dd2f-119">Přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="5dd2f-119">Invoice attachments</span></span>  
9. <span data-ttu-id="5dd2f-120">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-120">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="5dd2f-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-121">Click Add.</span></span>
11. <span data-ttu-id="5dd2f-122">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-122">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="5dd2f-123">Do pole Název zadejte Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-123">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="5dd2f-124">Obsah souboru</span><span class="sxs-lookup"><span data-stu-id="5dd2f-124">File content</span></span>  
13. <span data-ttu-id="5dd2f-125">V poli Typ položky vyberte Obsahuje.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-125">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="5dd2f-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-126">Click Add.</span></span>
15. <span data-ttu-id="5dd2f-127">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-127">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="5dd2f-128">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-128">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="5dd2f-129">Název souboru</span><span class="sxs-lookup"><span data-stu-id="5dd2f-129">File name</span></span>  
17. <span data-ttu-id="5dd2f-130">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-130">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="5dd2f-131">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-131">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-data-sources"></a><span data-ttu-id="5dd2f-132">Namapování nových prvků datového modelu na zdroje dat</span><span class="sxs-lookup"><span data-stu-id="5dd2f-132">Map new data model elements to data sources</span></span>
1. <span data-ttu-id="5dd2f-133">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-133">Click Map model to datasource.</span></span>
2. <span data-ttu-id="5dd2f-134">Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-134">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="5dd2f-135">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="5dd2f-135">InvoiceCustomer</span></span>  
    * <span data-ttu-id="5dd2f-136">Namapujeme nové prvky modelu na příslušné zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-136">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="5dd2f-137">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-137">Click Designer.</span></span>
4. <span data-ttu-id="5dd2f-138">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-138">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="5dd2f-139">Ve stromovém zobrazení rozbalte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-139">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="5dd2f-140">Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-140">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="5dd2f-141">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-141">Click Edit.</span></span>
8. <span data-ttu-id="5dd2f-142">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-142">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="5dd2f-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="5dd2f-143">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="5dd2f-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-144">Click Save.</span></span>
10. <span data-ttu-id="5dd2f-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-145">Close the page.</span></span>
11. <span data-ttu-id="5dd2f-146">Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-146">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="5dd2f-147">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-147">Click Edit.</span></span>
13. <span data-ttu-id="5dd2f-148">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-148">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="5dd2f-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="5dd2f-149">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="5dd2f-150">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-150">Click Save.</span></span>
15. <span data-ttu-id="5dd2f-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-151">Close the page.</span></span>
16. <span data-ttu-id="5dd2f-152">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-152">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="5dd2f-153">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-153">Click Edit.</span></span>
18. <span data-ttu-id="5dd2f-154">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-154">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="5dd2f-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="5dd2f-155">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="5dd2f-156">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-156">Click Save.</span></span>
20. <span data-ttu-id="5dd2f-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-157">Close the page.</span></span>
21. <span data-ttu-id="5dd2f-158">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-158">Click Save.</span></span>
22. <span data-ttu-id="5dd2f-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-159">Close the page.</span></span>
23. <span data-ttu-id="5dd2f-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-160">Close the page.</span></span>
24. <span data-ttu-id="5dd2f-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-161">Close the page.</span></span>
25. <span data-ttu-id="5dd2f-162">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-162">Click Change status.</span></span>
26. <span data-ttu-id="5dd2f-163">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-163">Click Complete.</span></span>
27. <span data-ttu-id="5dd2f-164">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5dd2f-164">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]