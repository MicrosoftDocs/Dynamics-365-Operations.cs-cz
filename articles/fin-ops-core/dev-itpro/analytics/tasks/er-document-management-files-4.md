---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví k souborů správy dokumentů ve výstupu elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5639a46c105e735d028e903513b4fcfb1f0d968
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142608"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="706a7-103">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="706a7-103">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="706a7-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="706a7-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="706a7-105">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="706a7-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="706a7-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití souboru pro správu dokumentů ve výstupech formátu (část 3: Vytvoření formátu).</span><span class="sxs-lookup"><span data-stu-id="706a7-106">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="706a7-107">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="706a7-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="706a7-108">Přidejte nezbytné přílohy pro prodejní objednávku z jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="706a7-108">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="706a7-109">Přejděte na Pohledávky > Faktury > Otevřené faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="706a7-109">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="706a7-110">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="706a7-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="706a7-111">Můžete například filtrovat v poli Faktura pomocí hodnoty „CIV-000148“.</span><span class="sxs-lookup"><span data-stu-id="706a7-111">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="706a7-112">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="706a7-112">CIV-000148</span></span>  
3. <span data-ttu-id="706a7-113">Klikněte na odkaz pro vybranou fakturu.</span><span class="sxs-lookup"><span data-stu-id="706a7-113">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="706a7-114">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="706a7-114">CIV-000148</span></span>  
4. <span data-ttu-id="706a7-115">Kliknutím přejdete na odkaz v poli Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="706a7-115">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="706a7-116">000148</span><span class="sxs-lookup"><span data-stu-id="706a7-116">000148</span></span>  
5. <span data-ttu-id="706a7-117">V poli Řádky nebo záhlaví vyberte možnost Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="706a7-117">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="706a7-118">Vyberte Záhlaví k označení, že to bude cíl pro přidání příloh.</span><span class="sxs-lookup"><span data-stu-id="706a7-118">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="706a7-119">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="706a7-119">Click Attach.</span></span>
    * <span data-ttu-id="706a7-120">Přidejte několik souborů jako přílohy k této prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="706a7-120">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="706a7-121">Použijte soubory typů dokumentů, které jsou podporovány správou dokumentů (s příponami DOCX, DPF, XML, JPG atd.).</span><span class="sxs-lookup"><span data-stu-id="706a7-121">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="706a7-122">Vyhledejte a vyberte soubory k připojení a dalšímu zpracování se související fakturou v elektronické zprávě elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="706a7-122">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="706a7-123">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="706a7-123">Click New.</span></span>
8. <span data-ttu-id="706a7-124">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="706a7-124">Click File.</span></span>
9. <span data-ttu-id="706a7-125">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="706a7-125">Click New.</span></span>
10. <span data-ttu-id="706a7-126">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="706a7-126">Click File.</span></span>
11. <span data-ttu-id="706a7-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="706a7-127">Close the page.</span></span>
12. <span data-ttu-id="706a7-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="706a7-128">Close the page.</span></span>
13. <span data-ttu-id="706a7-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="706a7-129">Close the page.</span></span>
14. <span data-ttu-id="706a7-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="706a7-130">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="706a7-131">Spuštění sestavy navržené pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="706a7-131">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="706a7-132">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="706a7-132">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="706a7-133">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="706a7-133">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="706a7-134">Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="706a7-134">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="706a7-135">Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".</span><span class="sxs-lookup"><span data-stu-id="706a7-135">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="706a7-136">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="706a7-136">Click Run.</span></span>
6. <span data-ttu-id="706a7-137">Rozbalte oddíl Záznamy k zahrnutí ().</span><span class="sxs-lookup"><span data-stu-id="706a7-137">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="706a7-138">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="706a7-138">Click Filter.</span></span>
8. <span data-ttu-id="706a7-139">Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="706a7-139">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="706a7-140">Zadejte hodnotu 000148 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="706a7-140">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="706a7-141">V poli kritérií "Prodejní objednávka" zadejte číslo objednávky 000148.</span><span class="sxs-lookup"><span data-stu-id="706a7-141">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="706a7-142">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="706a7-142">Click OK.</span></span>
11. <span data-ttu-id="706a7-143">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="706a7-143">Click OK.</span></span>
    * <span data-ttu-id="706a7-144">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="706a7-144">Review the generated output.</span></span> <span data-ttu-id="706a7-145">Všimněte si, že pro každou přílohu byl vytvořen jeden uzel XML.</span><span class="sxs-lookup"><span data-stu-id="706a7-145">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="706a7-146">Obsah přílohy je naplněna do výstupu XML v textovém formátu MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="706a7-146">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

