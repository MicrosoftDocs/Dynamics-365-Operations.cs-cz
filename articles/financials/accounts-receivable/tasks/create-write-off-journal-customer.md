---
title: Vytvoření odpisového deníku pro odběratele
description: Tento průvodce úkolem znázorňuje, jak nastavit parametry pro odpisy a potom odepsat transakce ze stránky Kolekce, stránky Otevřené faktury odběratele a stránky Odběratel.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cd576458bab1e4654d21773b581a5b0f726c928
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545503"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="1bd7e-103">Vytvoření odpisového deníku pro odběratele</span><span class="sxs-lookup"><span data-stu-id="1bd7e-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1bd7e-104">Tento průvodce úkolem znázorňuje, jak nastavit parametry pro odpisy a potom odepsat transakce ze stránky Kolekce, stránky Otevřené faktury odběratele a stránky Odběratel.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="1bd7e-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="1bd7e-106">Nastavení parametrů odpisu</span><span class="sxs-lookup"><span data-stu-id="1bd7e-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="1bd7e-107">Přejděte do nabídky Kredit a inkasa > Nastavení > Parametry pohledávek.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-107">Go to Credit and collections > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="1bd7e-108">Kliknutí na kartu Kolekce.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-108">Click the Collections tab.</span></span>
3. <span data-ttu-id="1bd7e-109">Rozbalte nebo sbalte oddíl Odpis.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-109">Expand or collapse the Write-off section.</span></span>
    * <span data-ttu-id="1bd7e-110">Odpisový deník je deník hlavní knihy, který bude obsahovat transakce odpisů, které jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-110">The Write-off journal is the general journal that will hold the write-off transactions that you create.</span></span>  
    * <span data-ttu-id="1bd7e-111">Pro každý odpis lze přiřadit kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="1bd7e-112">Toto výchozí nastavení můžete v době odpisu kdykoli přepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-112">You can override this default at the time of the write-off.</span></span>  
    * <span data-ttu-id="1bd7e-113">Nastavením hodnoty Ano umožníte oddělení DPH z původní transakce v odpisu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-113">Set this to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="1bd7e-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-114">Close the page.</span></span>
5. <span data-ttu-id="1bd7e-115">Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-115">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
    * <span data-ttu-id="1bd7e-116">Účet odpisu bude použit jako účet nákladů nebo úpravy rezerv v deníku hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="1bd7e-116">The write-off account will be used as the expense account or reserve adjustment in the general journal</span></span>   
6. <span data-ttu-id="1bd7e-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="1bd7e-118">Odpis zůstatku zákazníka ze stránky Splatné zůstatky</span><span class="sxs-lookup"><span data-stu-id="1bd7e-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="1bd7e-119">Přejděte do nabídky Kredit a inkasa > Inkasa > Splatné zůstatky.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-119">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="1bd7e-120">Označte řádek pro odběratele, který chcete odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="1bd7e-121">Označte například řádek obsahující společnost Birch Company.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="1bd7e-122">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-122">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="1bd7e-123">Klikněte na možnost Odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-123">Click Write off.</span></span>
5. <span data-ttu-id="1bd7e-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-124">Click OK.</span></span>
6. <span data-ttu-id="1bd7e-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-125">Close the page.</span></span>
7. <span data-ttu-id="1bd7e-126">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-126">Go to General ledger > Journal entries > General journals.</span></span>
8. <span data-ttu-id="1bd7e-127">Vyberte číslo dávky deníku pro deník, který obsahuje váš odpis.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-127">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="1bd7e-128">Je vytvořen jeden řádek pro storno zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="1bd7e-129">Jeden nebo více řádků jsou vytvořeny pro zaúčtování odpisů na účet odpisu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="1bd7e-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-130">Close the page.</span></span>
10. <span data-ttu-id="1bd7e-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="1bd7e-132">Odpisové transakce z inkasního formuláře.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="1bd7e-133">Přejděte do nabídky Kredit a inkasa > Inkasa > Splatné zůstatky.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-133">Go to Credit and collections > Collections > Aged balances.</span></span>
2. <span data-ttu-id="1bd7e-134">Vyberte jméno odběratele, který obsahuje transakce, které chcete odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="1bd7e-135">Vyberte například Cave Wholesales (US-004).</span><span class="sxs-lookup"><span data-stu-id="1bd7e-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="1bd7e-136">Označte řádek pro první transakci.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="1bd7e-137">Označte řádek pro druhou transakci.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="1bd7e-138">Klikněte na možnost Odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-138">Click Write off.</span></span>
6. <span data-ttu-id="1bd7e-139">Zadejte údaj "Pochybné pohledávky" do pole Komentář k důvodu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-139">In the Reason comment field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="1bd7e-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-140">Click OK.</span></span>
8. <span data-ttu-id="1bd7e-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-141">Close the page.</span></span>
9. <span data-ttu-id="1bd7e-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-142">Close the page.</span></span>
10. <span data-ttu-id="1bd7e-143">Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-143">Go to General ledger > Journal entries > General journals.</span></span>
11. <span data-ttu-id="1bd7e-144">Vyberte číslo dávky deníku pro deník, který obsahuje váš odpis.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-144">Select the journal batch number for the journal that contains your write-off.</span></span>
    * <span data-ttu-id="1bd7e-145">Je vytvořen jeden řádek pro storno zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="1bd7e-146">Jeden nebo více řádků jsou vytvořeny pro zaúčtování odpisů na účet odpisu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="1bd7e-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-147">Close the page.</span></span>
13. <span data-ttu-id="1bd7e-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="1bd7e-149">Odepsání faktury ze stránky Otevřené faktury odběratelů</span><span class="sxs-lookup"><span data-stu-id="1bd7e-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="1bd7e-150">Přejděte na Pohledávky > Faktury > Otevřené faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-150">Go to Accounts receivable > Invoices > Open customer invoices.</span></span>
2. <span data-ttu-id="1bd7e-151">Označte řádek pro fakturu.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-151">Mark the line for an invoice.</span></span> <span data-ttu-id="1bd7e-152">Například označte řádek pro CIV-000667.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="1bd7e-153">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-153">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="1bd7e-154">Klikněte na možnost Odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-154">Click Write off.</span></span>
5. <span data-ttu-id="1bd7e-155">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-155">Click OK.</span></span>
6. <span data-ttu-id="1bd7e-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="1bd7e-157">Odpis zůstatku odběratele ze strany zákazníka</span><span class="sxs-lookup"><span data-stu-id="1bd7e-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="1bd7e-158">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-158">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="1bd7e-159">Výběr účtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-159">Select a customer account.</span></span> <span data-ttu-id="1bd7e-160">Vyberte například USA-001 (Maloobchod Contoso pro San Diego).</span><span class="sxs-lookup"><span data-stu-id="1bd7e-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="1bd7e-161">V podokně akcí klikněte na možnost Kolekce.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-161">On the Action Pane, click Collect.</span></span>
4. <span data-ttu-id="1bd7e-162">Klikněte na možnost Odepsat.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-162">Click Write off.</span></span>
5. <span data-ttu-id="1bd7e-163">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-163">Click OK.</span></span>
6. <span data-ttu-id="1bd7e-164">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1bd7e-164">Close the page.</span></span>

