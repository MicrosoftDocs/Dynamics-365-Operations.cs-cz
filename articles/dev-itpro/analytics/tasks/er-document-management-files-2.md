--- 
title: "Rozšíření datového modelu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)"
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: ebbd442c9f69290dc995c05462ca70b554f7d9f2
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a><span data-ttu-id="317bd-103">Rozšíření datového modelu k použití souborů pro správu dokumentů ve formátech výstupu pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="317bd-103">Extend data model to use Document Management files in format outputs for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="317bd-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="317bd-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="317bd-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="317bd-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="317bd-106">K dokončení těchto kroků je nutné nejprve provést kroky v průvodci záznamem úloh "Soubory správy dokumentů použití ER soubory ve výstupech formátu (Část 1: Příprava datového modelu).</span><span class="sxs-lookup"><span data-stu-id="317bd-106">To complete these steps, you must first complete the steps in the “ER Use Document Management files in format outputs (Part 1: Prepare data model)” task guide.</span></span>

<span data-ttu-id="317bd-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="317bd-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a><span data-ttu-id="317bd-108">Rozšíření datového modelu na prezentaci souborů správy dokumentů</span><span class="sxs-lookup"><span data-stu-id="317bd-108">Extend data model to present the Document Management files in it</span></span>
1. <span data-ttu-id="317bd-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="317bd-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="317bd-110">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="317bd-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="317bd-111">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="317bd-111">In the tree, expand 'Customer invoice model'.</span></span>
4. <span data-ttu-id="317bd-112">Ve stromu vyberte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="317bd-112">In the tree, select 'Customer invoice model\Customer invoice model (custom)'.</span></span>
5. <span data-ttu-id="317bd-113">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="317bd-113">Click Designer.</span></span>
6. <span data-ttu-id="317bd-114">Ve stromovém zobrazení vyberte možnost Faktura odběratele (InvoiceCustomer).</span><span class="sxs-lookup"><span data-stu-id="317bd-114">In the tree, select 'Customer invoice(InvoiceCustomer)'.</span></span>
    * <span data-ttu-id="317bd-115">Rozšíříme tento datový model, tak aby v něm byly vystaveny všechny soubory, které byly připojeny k prodejní objednávce, která se vztahuje k elektronickému zpracování faktur.</span><span class="sxs-lookup"><span data-stu-id="317bd-115">We will extend this data model to expose in it any files that have been attached to a sales order that is related to an electronically processing invoice.</span></span>  
7. <span data-ttu-id="317bd-116">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="317bd-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="317bd-117">Do pole Název zadejte Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="317bd-117">In the Name field, type 'Invoice attachments'.</span></span>
    * <span data-ttu-id="317bd-118">Přílohy faktury</span><span class="sxs-lookup"><span data-stu-id="317bd-118">Invoice attachments</span></span>  
9. <span data-ttu-id="317bd-119">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="317bd-119">In the Item type field, select 'Record list'.</span></span>
10. <span data-ttu-id="317bd-120">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="317bd-120">Click Add.</span></span>
11. <span data-ttu-id="317bd-121">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="317bd-121">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="317bd-122">Do pole Název zadejte Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="317bd-122">In the Name field, type 'File content'.</span></span>
    * <span data-ttu-id="317bd-123">Obsah souboru</span><span class="sxs-lookup"><span data-stu-id="317bd-123">File content</span></span>  
13. <span data-ttu-id="317bd-124">V poli Typ položky vyberte Obsahuje.</span><span class="sxs-lookup"><span data-stu-id="317bd-124">In the Item type field, select 'Container'.</span></span>
14. <span data-ttu-id="317bd-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="317bd-125">Click Add.</span></span>
15. <span data-ttu-id="317bd-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="317bd-126">Click New to open the drop dialog.</span></span>
16. <span data-ttu-id="317bd-127">Do pole Název zadejte Název souboru.</span><span class="sxs-lookup"><span data-stu-id="317bd-127">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="317bd-128">Název souboru</span><span class="sxs-lookup"><span data-stu-id="317bd-128">File name</span></span>  
17. <span data-ttu-id="317bd-129">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="317bd-129">In the Item type field, select 'String'.</span></span>
18. <span data-ttu-id="317bd-130">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="317bd-130">Click Add.</span></span>

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-data-sources"></a><span data-ttu-id="317bd-131">Mapování nových prvků datového modelu do zdrojových dat aplikace Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="317bd-131">Map new data model elements to Dynamics 365 for Finance and Operations data sources</span></span>
1. <span data-ttu-id="317bd-132">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="317bd-132">Click Map model to datasource.</span></span>
2. <span data-ttu-id="317bd-133">Použijte rychlý filtr k filtrování v poli Definice s hodnotou 'InvoiceCustomer'.</span><span class="sxs-lookup"><span data-stu-id="317bd-133">Use the Quick Filter to filter on the Definition field with a value of 'InvoiceCustomer'.</span></span>
    * <span data-ttu-id="317bd-134">InvoiceCustomer</span><span class="sxs-lookup"><span data-stu-id="317bd-134">InvoiceCustomer</span></span>  
    * <span data-ttu-id="317bd-135">Namapujeme nové prvky modelu na příslušné zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="317bd-135">We will map new model elements to appropriate data sources.</span></span>  
3. <span data-ttu-id="317bd-136">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="317bd-136">Click Designer.</span></span>
4. <span data-ttu-id="317bd-137">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="317bd-137">In the tree, select 'Invoice attachments'.</span></span>
5. <span data-ttu-id="317bd-138">Ve stromovém zobrazení rozbalte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="317bd-138">In the tree, expand 'Invoice attachments'.</span></span>
6. <span data-ttu-id="317bd-139">Ve stromovém zobrazení vyberte možnost Přílohy faktury\Název souboru.</span><span class="sxs-lookup"><span data-stu-id="317bd-139">In the tree, select 'Invoice attachments\File name'.</span></span>
7. <span data-ttu-id="317bd-140">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="317bd-140">Click Edit.</span></span>
8. <span data-ttu-id="317bd-141">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span><span class="sxs-lookup"><span data-stu-id="317bd-141">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.</span></span>
    * <span data-ttu-id="317bd-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span><span class="sxs-lookup"><span data-stu-id="317bd-142">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'</span></span>  
9. <span data-ttu-id="317bd-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="317bd-143">Click Save.</span></span>
10. <span data-ttu-id="317bd-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-144">Close the page.</span></span>
11. <span data-ttu-id="317bd-145">Ve stromové struktuře vyberte Přílohy faktury\Obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="317bd-145">In the tree, select 'Invoice attachments\File content'.</span></span>
12. <span data-ttu-id="317bd-146">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="317bd-146">Click Edit.</span></span>
13. <span data-ttu-id="317bd-147">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span><span class="sxs-lookup"><span data-stu-id="317bd-147">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.</span></span>
    * <span data-ttu-id="317bd-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span><span class="sxs-lookup"><span data-stu-id="317bd-148">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'</span></span>  
14. <span data-ttu-id="317bd-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="317bd-149">Click Save.</span></span>
15. <span data-ttu-id="317bd-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-150">Close the page.</span></span>
16. <span data-ttu-id="317bd-151">Ve stromovém zobrazení vyberte možnost Přílohy faktury.</span><span class="sxs-lookup"><span data-stu-id="317bd-151">In the tree, select 'Invoice attachments'.</span></span>
17. <span data-ttu-id="317bd-152">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="317bd-152">Click Edit.</span></span>
18. <span data-ttu-id="317bd-153">Do pole Vzorec napište 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span><span class="sxs-lookup"><span data-stu-id="317bd-153">In the Formula field, enter 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.</span></span>
    * <span data-ttu-id="317bd-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span><span class="sxs-lookup"><span data-stu-id="317bd-154">CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'</span></span>  
19. <span data-ttu-id="317bd-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="317bd-155">Click Save.</span></span>
20. <span data-ttu-id="317bd-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-156">Close the page.</span></span>
21. <span data-ttu-id="317bd-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="317bd-157">Click Save.</span></span>
22. <span data-ttu-id="317bd-158">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-158">Close the page.</span></span>
23. <span data-ttu-id="317bd-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-159">Close the page.</span></span>
24. <span data-ttu-id="317bd-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="317bd-160">Close the page.</span></span>
25. <span data-ttu-id="317bd-161">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="317bd-161">Click Change status.</span></span>
26. <span data-ttu-id="317bd-162">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="317bd-162">Click Complete.</span></span>
27. <span data-ttu-id="317bd-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="317bd-163">Click OK.</span></span>


