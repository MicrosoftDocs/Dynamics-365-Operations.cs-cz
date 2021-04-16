---
title: Vytváření faktur prodejních objednávek
description: Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837098"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="328d0-103">Vytváření faktur prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="328d0-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="328d0-104">Tento průvodce úkolem popisuje zásady fakturace prodejní objednávky, včetně sloučení faktur a dávkového zpracování.</span><span class="sxs-lookup"><span data-stu-id="328d0-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="328d0-105">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="328d0-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="328d0-106">Vytvoření faktury z prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="328d0-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="328d0-107">Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Dodáno ale bez vyfakturovaných prodejních objednávek**.</span><span class="sxs-lookup"><span data-stu-id="328d0-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="328d0-108">Vyberte ze seznamu prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="328d0-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="328d0-109">V **Podokně akcí** klikněte na **Faktura > Generovat > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="328d0-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="328d0-110">Všimněte si, že tato prodejní objednávka má přidruženo více dodacích listů.</span><span class="sxs-lookup"><span data-stu-id="328d0-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="328d0-111">Zde se zobrazí pouze slovo <multiple> namísto čísla dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="328d0-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="328d0-112">Rozbalte sekci **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="328d0-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="328d0-113">Zaúčtování musí být pro zaúčtování faktury nastaveno na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="328d0-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="328d0-114">Lze také vypnout zaúčtování fakturu pouze vytisknout.</span><span class="sxs-lookup"><span data-stu-id="328d0-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="328d0-115">Stejného výsledku však lze dosáhnout pomocí vytvoření faktury proforma namísto faktury.</span><span class="sxs-lookup"><span data-stu-id="328d0-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="328d0-116">Tato možnost se využívá pro dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="328d0-116">This option is used for batch jobs.</span></span> <span data-ttu-id="328d0-117">Dotaz se spustí při spuštění dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="328d0-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="328d0-118">V poli **Tisk** vyberte možnost Po.</span><span class="sxs-lookup"><span data-stu-id="328d0-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="328d0-119">Vyberte možnost **Ano** pro **Tisk faktury**.</span><span class="sxs-lookup"><span data-stu-id="328d0-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="328d0-120">Správu tisku umožňuje vytisknout více kopií faktury a také odesílat faktury prostřednictvím e-mailu jako soubor PDF.</span><span class="sxs-lookup"><span data-stu-id="328d0-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="328d0-121">Vyberte možnost Souhrn v poli **Tisk nákladů**.</span><span class="sxs-lookup"><span data-stu-id="328d0-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="328d0-122">V poli **Zkontrolovat limit** úvěru vyberte 'Zůstatek'.</span><span class="sxs-lookup"><span data-stu-id="328d0-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="328d0-123">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="328d0-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="328d0-124">Sloučení objednávek do jedné faktury</span><span class="sxs-lookup"><span data-stu-id="328d0-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="328d0-125">Přejděte na **Navigační podokno > Moduly > Pohledávky > Objednávky > Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="328d0-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="328d0-126">Vyhledejte zákazníka, který má více otevřených faktur.</span><span class="sxs-lookup"><span data-stu-id="328d0-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="328d0-127">Vyberte více otevřených prodejních objednávek od stejného odběratele.</span><span class="sxs-lookup"><span data-stu-id="328d0-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="328d0-128">V **Podokně akcí** klikněte na **Faktura > Generovat > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="328d0-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="328d0-129">Rozbalte sekci **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="328d0-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="328d0-130">V poli **Množství** vyberte možnost „Vše“.</span><span class="sxs-lookup"><span data-stu-id="328d0-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="328d0-131">Existují dvě faktury, které jsou uvedeny v přehledu.</span><span class="sxs-lookup"><span data-stu-id="328d0-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="328d0-132">Nyní je sloučíme do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="328d0-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="328d0-133">V poli **Souhrnná aktualizace pro** vyberte Účet faktury.</span><span class="sxs-lookup"><span data-stu-id="328d0-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="328d0-134">Klikněte na **Uspořádat** pro sloučení prodejních objednávky do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="328d0-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="328d0-135">Dvě prodejních objednávky jsou nyní sloučeny do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="328d0-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="328d0-136">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="328d0-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="328d0-137">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="328d0-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="328d0-138">Zaúčtování faktur do dávky</span><span class="sxs-lookup"><span data-stu-id="328d0-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="328d0-139">Přejděte na **Navigační podokno > Moduly > Pohledávky > Faktury > Dávková fakturace > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="328d0-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="328d0-140">Klepněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="328d0-140">Click **Select**.</span></span>
3. <span data-ttu-id="328d0-141">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="328d0-141">Click **OK**.</span></span>
4. <span data-ttu-id="328d0-142">Klepněte na možnost **Dávka**.</span><span class="sxs-lookup"><span data-stu-id="328d0-142">Click **Batch**.</span></span>
5. <span data-ttu-id="328d0-143">Vyberte možnost **Ano** v části **Dávkové zpracování**.</span><span class="sxs-lookup"><span data-stu-id="328d0-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="328d0-144">Klikněte na **Opakování**.</span><span class="sxs-lookup"><span data-stu-id="328d0-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="328d0-145">Vyberte **Dny**.</span><span class="sxs-lookup"><span data-stu-id="328d0-145">Select **Days**.</span></span>
8. <span data-ttu-id="328d0-146">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="328d0-146">Click **OK**.</span></span>
9. <span data-ttu-id="328d0-147">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="328d0-147">Click **OK**.</span></span>
10. <span data-ttu-id="328d0-148">Klepněte na možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="328d0-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="328d0-149">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="328d0-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]