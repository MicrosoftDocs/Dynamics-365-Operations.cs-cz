---
title: Vytváření plateb pro odběratele, který má zmocnění k přímému debetu
description: Tato procedura ukazuje, jak generovat soubor plateb přímého debetu ISO20022 pro odběratele, který má nakonfigurován přímý debet a fakturu k zaplacení.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441255"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="b4e5d-103">Vytváření plateb pro odběratele, který má zmocnění k přímému debetu</span><span class="sxs-lookup"><span data-stu-id="b4e5d-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b4e5d-104">Tato procedura ukazuje, jak generovat soubor plateb přímého debetu ISO20022 pro odběratele, který má nakonfigurován přímý debet a fakturu k zaplacení.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="b4e5d-105">Vytvoření a zaúčtování faktury je volitelné.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="b4e5d-106">Namísto faktury k zaplacení můžete vybrat zmocnění v deníku před generováním souboru plateb, na podporu scénáře zálohy odběratele.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="b4e5d-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="b4e5d-108">Toto je pátá z pěti procedur, které demonstrují proces plateb odběratele pomocí konfigurací elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="b4e5d-109">Před dokončením tohoto úkolu je třeba dokončit předchozí úkoly.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="b4e5d-110">Je nutné nejprve importovat konfigurace elektronického výkaznictví plateb odběratele, konfigurovat metodu plateb a nastavit informace o společnosti a odběrateli.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="b4e5d-111">Zaúčtování volné faktury s informacemi o přímém debetu</span><span class="sxs-lookup"><span data-stu-id="b4e5d-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="b4e5d-112">Přejděte na Pohledávky > Faktury > Všechny volné faktury.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="b4e5d-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-113">Click New.</span></span>
3. <span data-ttu-id="b4e5d-114">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="b4e5d-115">Vyberte například DE-010.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="b4e5d-116">V poli Metody platby zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="b4e5d-117">Například</span><span class="sxs-lookup"><span data-stu-id="b4e5d-117">For example.</span></span> <span data-ttu-id="b4e5d-118">Vyberte Elektronicky.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-118">select Electronic.</span></span>  
5. <span data-ttu-id="b4e5d-119">V poli ID zmocnění k přímému debetu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="b4e5d-120">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-120">Click Add line.</span></span>
7. <span data-ttu-id="b4e5d-121">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="b4e5d-122">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="b4e5d-123">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="b4e5d-124">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-124">Click Post.</span></span>
11. <span data-ttu-id="b4e5d-125">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="b4e5d-126">Vytvořte platby</span><span class="sxs-lookup"><span data-stu-id="b4e5d-126">Create a payment</span></span>
1. <span data-ttu-id="b4e5d-127">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b4e5d-128">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-128">Click New.</span></span>
3. <span data-ttu-id="b4e5d-129">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="b4e5d-130">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-130">Click Lines.</span></span>
5. <span data-ttu-id="b4e5d-131">Klikněte na Návrh platby.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="b4e5d-132">Klikněte na Vytvořit návrh plateb.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="b4e5d-133">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="b4e5d-134">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-134">Click Filter.</span></span>
9. <span data-ttu-id="b4e5d-135">V seznamu vyberte řádek v tabulce Transakce zákazníka a v poli Metoda platby.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="b4e5d-136">Můžete použít libovolná kritéria pro výběr transakcí odběratele k zaplacení.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="b4e5d-137">V tomto příkladu jako metodu platby k filtrování transakcí použijte Elektronicky.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="b4e5d-138">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="b4e5d-139">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-139">Click OK.</span></span>
12. <span data-ttu-id="b4e5d-140">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-140">Click OK.</span></span>
13. <span data-ttu-id="b4e5d-141">Klikněte na Vytvořit platby.</span><span class="sxs-lookup"><span data-stu-id="b4e5d-141">Click Create payments.</span></span>
