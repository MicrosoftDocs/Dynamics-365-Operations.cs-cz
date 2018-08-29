--- 
title: "Rozšíření datových modelů k použití souborů pro správu dokumentů ve výstupu elektronického výkaznictví"
description: "Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8363dd2af728577175a620d7b645d90cea84803a
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="extend-data-models-to-use-document-management-files-in-er-output"></a><span data-ttu-id="1eab0-103">Rozšíření datových modelů k použití souborů pro správu dokumentů ve výstupu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="1eab0-103">Extend data models to use Document Management files in ER output</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1eab0-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="1eab0-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="1eab0-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="1eab0-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="1eab0-106">K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).</span><span class="sxs-lookup"><span data-stu-id="1eab0-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="1eab0-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="1eab0-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="1eab0-108">Rozšíření datového modelu na prezentaci souborů správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="1eab0-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="1eab0-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="1eab0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1eab0-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="1eab0-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1eab0-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="1eab0-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="1eab0-112">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="1eab0-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="1eab0-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="1eab0-113">Click Designer.</span></span>
6. <span data-ttu-id="1eab0-114">Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="1eab0-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="1eab0-115">Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="1eab0-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="1eab0-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1eab0-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="1eab0-117">Do pole Název zadejte Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="1eab0-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="1eab0-118">Přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="1eab0-118">Invoice attachments</span></span>  
9. <span data-ttu-id="1eab0-119">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="1eab0-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="1eab0-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1eab0-120">Click Add.</span></span>
11. <span data-ttu-id="1eab0-121">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1eab0-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="1eab0-122">Do pole Název zadejte Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="1eab0-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="1eab0-123">Obsah souboru</span><span class="sxs-lookup"><span data-stu-id="1eab0-123">File content</span></span>  
13. <span data-ttu-id="1eab0-124">V poli Typ položky vyberte Obsahuje.</span><span class="sxs-lookup"><span data-stu-id="1eab0-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="1eab0-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1eab0-125">Click Add.</span></span>
15. <span data-ttu-id="1eab0-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1eab0-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="1eab0-127">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="1eab0-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="1eab0-128">Název souboru</span><span class="sxs-lookup"><span data-stu-id="1eab0-128">File name</span></span>  
17. <span data-ttu-id="1eab0-129">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="1eab0-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="1eab0-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1eab0-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="1eab0-131">Mapování nových prvků datového modelu do zdrojových dat aplikace Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="1eab0-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="1eab0-132">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="1eab0-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="1eab0-133">Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="1eab0-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="1eab0-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="1eab0-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="1eab0-135">Namapujeme nové prvky modelu na příslušné zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="1eab0-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="1eab0-136">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="1eab0-136">Click Designer.</span></span>
4. <span data-ttu-id="1eab0-137">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="1eab0-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="1eab0-138">Ve stromovém zobrazení rozbalte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="1eab0-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="1eab0-139">Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.</span><span class="sxs-lookup"><span data-stu-id="1eab0-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="1eab0-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-140">Click Edit.</span></span>
8. <span data-ttu-id="1eab0-141">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="1eab0-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="1eab0-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="1eab0-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="1eab0-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-143">Click Save.</span></span>
10. <span data-ttu-id="1eab0-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-144">Close the page.</span></span>
11. <span data-ttu-id="1eab0-145">Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="1eab0-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="1eab0-146">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-146">Click Edit.</span></span>
13. <span data-ttu-id="1eab0-147">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="1eab0-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="1eab0-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="1eab0-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="1eab0-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-149">Click Save.</span></span>
15. <span data-ttu-id="1eab0-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-150">Close the page.</span></span>
16. <span data-ttu-id="1eab0-151">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="1eab0-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="1eab0-152">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-152">Click Edit.</span></span>
18. <span data-ttu-id="1eab0-153">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="1eab0-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="1eab0-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="1eab0-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="1eab0-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-155">Click Save.</span></span>
20. <span data-ttu-id="1eab0-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-156">Close the page.</span></span>
21. <span data-ttu-id="1eab0-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-157">Click Save.</span></span>
22. <span data-ttu-id="1eab0-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-158">Close the page.</span></span>
23. <span data-ttu-id="1eab0-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-159">Close the page.</span></span>
24. <span data-ttu-id="1eab0-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1eab0-160">Close the page.</span></span>
25. <span data-ttu-id="1eab0-161">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="1eab0-161">Click Change status.</span></span>
26. <span data-ttu-id="1eab0-162">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="1eab0-162">Click Complete.</span></span>
27. <span data-ttu-id="1eab0-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1eab0-163">Click OK.</span></span>


