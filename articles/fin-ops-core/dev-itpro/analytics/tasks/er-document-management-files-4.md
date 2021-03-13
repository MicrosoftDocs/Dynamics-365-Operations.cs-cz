---
title: Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)
description: Toto téma popisuje, jak nakonfigurovat formát elektronického výkaznictví na použití souborů správy dokumentů ve výstupu ER. (část 4)
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d437b31b8a55f345ebc3567bc8c6a2c5ecfd2eec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092509"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a><span data-ttu-id="9fd91-104">Elektronické výkaznictví – Používání souborů pro správu dokumentů ve formátech výstupu (část 4 - Spuštění formátu)</span><span class="sxs-lookup"><span data-stu-id="9fd91-104">ER Use Document Management files in format outputs (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fd91-105">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat formát elektronického výkaznictví (ER) k souborů správy dokumentů (příloh) ve výstupu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9fd91-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to use Document Management files (attachments) in ER output.</span></span> <span data-ttu-id="9fd91-106">Tyto kroky lze provést v rámci společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="9fd91-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="9fd91-107">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití souboru pro správu dokumentů ve výstupech formátu (část 3: Vytvoření formátu).</span><span class="sxs-lookup"><span data-stu-id="9fd91-107">To complete these steps, you must first complete the steps in the "ER Use Document Management files in format outputs (Part 3: Create format)" procedure.</span></span>

<span data-ttu-id="9fd91-108">Tento postup je určený pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="9fd91-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a><span data-ttu-id="9fd91-109">Přidejte nezbytné přílohy pro prodejní objednávku z jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="9fd91-109">Add necessary attachments for sales order of a single invoice</span></span>
1. <span data-ttu-id="9fd91-110">Přejděte na Pohledávky > Faktury > Otevřené faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="9fd91-110">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="9fd91-111">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="9fd91-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9fd91-112">Můžete například filtrovat v poli Faktura pomocí hodnoty „CIV-000148“.</span><span class="sxs-lookup"><span data-stu-id="9fd91-112">For example, filter on the Invoice field with a value of 'CIV-000148'.</span></span>
    * <span data-ttu-id="9fd91-113">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="9fd91-113">CIV-000148</span></span>  
3. <span data-ttu-id="9fd91-114">Klikněte na odkaz pro vybranou fakturu.</span><span class="sxs-lookup"><span data-stu-id="9fd91-114">Click to follow the selected invoice's link.</span></span>
    * <span data-ttu-id="9fd91-115">CIV-000148</span><span class="sxs-lookup"><span data-stu-id="9fd91-115">CIV-000148</span></span>  
4. <span data-ttu-id="9fd91-116">Kliknutím přejdete na odkaz v poli Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="9fd91-116">Click to follow the link in the Sales order field.</span></span>
    * <span data-ttu-id="9fd91-117">000148</span><span class="sxs-lookup"><span data-stu-id="9fd91-117">000148</span></span>  
5. <span data-ttu-id="9fd91-118">V poli Řádky nebo záhlaví vyberte možnost Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="9fd91-118">In the Lines or header field, select the option of Header.</span></span>
    * <span data-ttu-id="9fd91-119">Vyberte Záhlaví k označení, že to bude cíl pro přidání příloh.</span><span class="sxs-lookup"><span data-stu-id="9fd91-119">Select Header to indicate that this will be the target for adding attachments.</span></span>  
6. <span data-ttu-id="9fd91-120">Klikněte na možnost Připojit.</span><span class="sxs-lookup"><span data-stu-id="9fd91-120">Click Attach.</span></span>
    * <span data-ttu-id="9fd91-121">Přidejte několik souborů jako přílohy k této prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="9fd91-121">Add a few files as attachments for this sales order.</span></span> <span data-ttu-id="9fd91-122">Použijte soubory typů dokumentů, které jsou podporovány správou dokumentů (s příponami DOCX, DPF, XML, JPG atd.).</span><span class="sxs-lookup"><span data-stu-id="9fd91-122">Use the files of the document types that are supported by the Document Management (with file extensions DOCX, DPF, XML, JPG, etc.).</span></span> <span data-ttu-id="9fd91-123">Vyhledejte a vyberte soubory k připojení a dalšímu zpracování se související fakturou v elektronické zprávě elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9fd91-123">Browse and select files to be attached and further processed with the related invoice in the ER electronic message.</span></span>  
7. <span data-ttu-id="9fd91-124">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9fd91-124">Click New.</span></span>
8. <span data-ttu-id="9fd91-125">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="9fd91-125">Click File.</span></span>
9. <span data-ttu-id="9fd91-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9fd91-126">Click New.</span></span>
10. <span data-ttu-id="9fd91-127">Klepněte na volby Soubor.</span><span class="sxs-lookup"><span data-stu-id="9fd91-127">Click File.</span></span>
11. <span data-ttu-id="9fd91-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9fd91-128">Close the page.</span></span>
12. <span data-ttu-id="9fd91-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9fd91-129">Close the page.</span></span>
13. <span data-ttu-id="9fd91-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9fd91-130">Close the page.</span></span>
14. <span data-ttu-id="9fd91-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9fd91-131">Close the page.</span></span>

## <a name="run-the-designed-report-for-the-selected-invoice"></a><span data-ttu-id="9fd91-132">Spuštění sestavy navržené pro vybranou fakturu</span><span class="sxs-lookup"><span data-stu-id="9fd91-132">Run the designed report for the selected invoice</span></span>
1. <span data-ttu-id="9fd91-133">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="9fd91-133">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9fd91-134">Ve stromovém zobrazení rozbalte možnost Model faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="9fd91-134">In the tree, expand 'Customer invoice model'.</span></span>
3. <span data-ttu-id="9fd91-135">Ve stromu rozbalte položku "Model faktury odběratele\Model faktury odběratele (vlastní)".</span><span class="sxs-lookup"><span data-stu-id="9fd91-135">In the tree, expand 'Customer invoice model\Customer invoice model (custom)'.</span></span>
4. <span data-ttu-id="9fd91-136">Ve stromové struktuře vyberte "Model faktury odběratele\Model faktury odběratele (vlastní)\Zpráva s ukázkou elektronické faktury".</span><span class="sxs-lookup"><span data-stu-id="9fd91-136">In the tree, select 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.</span></span>
5. <span data-ttu-id="9fd91-137">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="9fd91-137">Click Run.</span></span>
6. <span data-ttu-id="9fd91-138">Rozbalte oddíl Záznamy k zahrnutí ().</span><span class="sxs-lookup"><span data-stu-id="9fd91-138">Expand the Records to include () section.</span></span>
7. <span data-ttu-id="9fd91-139">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="9fd91-139">Click Filter.</span></span>
8. <span data-ttu-id="9fd91-140">Vyberte řádek deníku faktury odběratele a pole Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="9fd91-140">Select the row of the Customer invoice journal and the Sales order field.</span></span>
9. <span data-ttu-id="9fd91-141">Zadejte hodnotu 000148 do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="9fd91-141">In the Criteria field, type '000148'.</span></span>
    * <span data-ttu-id="9fd91-142">V poli kritérií "Prodejní objednávka" zadejte číslo objednávky 000148.</span><span class="sxs-lookup"><span data-stu-id="9fd91-142">In the criteria "Sales order" field, type the order number 000148.</span></span>  
10. <span data-ttu-id="9fd91-143">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9fd91-143">Click OK.</span></span>
11. <span data-ttu-id="9fd91-144">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9fd91-144">Click OK.</span></span>
    * <span data-ttu-id="9fd91-145">Prohlédněte si generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="9fd91-145">Review the generated output.</span></span> <span data-ttu-id="9fd91-146">Všimněte si, že pro každou přílohu byl vytvořen jeden uzel XML.</span><span class="sxs-lookup"><span data-stu-id="9fd91-146">Note that for each attachment a single XML node has been created.</span></span> <span data-ttu-id="9fd91-147">Obsah přílohy je naplněna do výstupu XML v textovém formátu MIME (base64).</span><span class="sxs-lookup"><span data-stu-id="9fd91-147">The attachment's content is populated to the XML output in MIME (base64) text format.</span></span>  

