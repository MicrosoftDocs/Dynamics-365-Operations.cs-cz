---
title: Vytváření faktur prodejních objednávek
description: Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565199"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="0777e-103">Vytváření faktur prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="0777e-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0777e-104">Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="0777e-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="0777e-105">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="0777e-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="0777e-106">Vytvoření faktury z prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="0777e-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="0777e-107">Přejděte na Pohledávky > Objednávky > Dodáno ale bez vyfakturovaných prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="0777e-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="0777e-108">Vyberte ze seznamu prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="0777e-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="0777e-109">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0777e-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="0777e-110">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0777e-110">Click Invoice.</span></span>
    * <span data-ttu-id="0777e-111">Všimněte si, že tato prodejní objednávka má přidruženo více dodacích listů.</span><span class="sxs-lookup"><span data-stu-id="0777e-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="0777e-112">Zde se zobrazí pouze slovo <multiple> namísto čísla dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="0777e-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="0777e-113">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="0777e-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="0777e-114">Zaúčtování musí být pro zaúčtování faktury nastaveno na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="0777e-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="0777e-115">Lze také vypnout zaúčtování fakturu pouze vytisknout.</span><span class="sxs-lookup"><span data-stu-id="0777e-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="0777e-116">Stejného výsledku však lze dosáhnout pomocí vytvoření faktury proforma namísto faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="0777e-117">Tato možnost se využívá pro dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="0777e-117">This option is used for batch jobs.</span></span> <span data-ttu-id="0777e-118">Dotaz se spustí při spuštění dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="0777e-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="0777e-119">V poli Tisk vyberte možnost Po.</span><span class="sxs-lookup"><span data-stu-id="0777e-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="0777e-120">Vyberte možnost Ano pro tisk faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="0777e-121">Správu tisku umožňuje vytisknout více kopií faktury a také odesílat faktury prostřednictvím e-mailu jako soubor PDF.</span><span class="sxs-lookup"><span data-stu-id="0777e-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="0777e-122">Vyberte možnost Souhrn v poli Tisk nákladů.</span><span class="sxs-lookup"><span data-stu-id="0777e-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="0777e-123">V poli Zkontrolovat limit úvěru vyberte 'Zůstatek'.</span><span class="sxs-lookup"><span data-stu-id="0777e-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="0777e-124">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="0777e-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="0777e-125">Sloučení objednávek do jedné faktury</span><span class="sxs-lookup"><span data-stu-id="0777e-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="0777e-126">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="0777e-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0777e-127">Vyhledejte zákazníka, který má více otevřených faktur.</span><span class="sxs-lookup"><span data-stu-id="0777e-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="0777e-128">Vyberte otevřenou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="0777e-128">Select an open sales order.</span></span>
4. <span data-ttu-id="0777e-129">Vyberte jinou otevřenou prodejní objednávku pro stejného odběratele.</span><span class="sxs-lookup"><span data-stu-id="0777e-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="0777e-130">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="0777e-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="0777e-131">Klepněte na Faktura.</span><span class="sxs-lookup"><span data-stu-id="0777e-131">Click Invoice.</span></span>
7. <span data-ttu-id="0777e-132">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="0777e-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="0777e-133">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="0777e-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="0777e-134">Existují dvě faktury, které jsou uvedeny v přehledu.</span><span class="sxs-lookup"><span data-stu-id="0777e-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="0777e-135">Nyní je sloučíme do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="0777e-136">V poli Souhrnná aktualizace pro vyberte Účet faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="0777e-137">Klikněte na Účet faktury pro sloučení prodejních objednávky do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="0777e-138">Dvě prodejních objednávky jsou nyní sloučeny do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="0777e-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="0777e-139">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="0777e-139">Click Cancel.</span></span>
12. <span data-ttu-id="0777e-140">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="0777e-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="0777e-141">Zaúčtování faktur do dávky</span><span class="sxs-lookup"><span data-stu-id="0777e-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="0777e-142">Přejděte na Pohledávky > Faktury > Dávková fakturace > Faktura.</span><span class="sxs-lookup"><span data-stu-id="0777e-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="0777e-143">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="0777e-143">Click Select.</span></span>
3. <span data-ttu-id="0777e-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0777e-144">Click OK.</span></span>
4. <span data-ttu-id="0777e-145">Klepněte na možnost Dávka.</span><span class="sxs-lookup"><span data-stu-id="0777e-145">Click Batch.</span></span>
5. <span data-ttu-id="0777e-146">Klepněte na hodnotu Ano, chcete-li povolit dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="0777e-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="0777e-147">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="0777e-147">Click Recurrence.</span></span>
7. <span data-ttu-id="0777e-148">Vyberte Dny</span><span class="sxs-lookup"><span data-stu-id="0777e-148">Select Days</span></span>
8. <span data-ttu-id="0777e-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0777e-149">Click OK.</span></span>
9. <span data-ttu-id="0777e-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0777e-150">Click OK.</span></span>
10. <span data-ttu-id="0777e-151">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="0777e-151">Click Cancel.</span></span>
11. <span data-ttu-id="0777e-152">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="0777e-152">Click Yes.</span></span>

