---
title: Přehled plateb odběratele
description: Tento průvodce záznamem úloh vás provede různými metodami zadání plateb odběratele.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566126"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="8eaf8-103">Přehled plateb odběratele</span><span class="sxs-lookup"><span data-stu-id="8eaf8-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8eaf8-104">Tento průvodce záznamem úloh vás provede různými metodami zadání plateb odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="8eaf8-105">Tento úkol používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="8eaf8-106">Přejděte na Pohledávky > Platby > Deník plateb.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8eaf8-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-107">Click New.</span></span>
3. <span data-ttu-id="8eaf8-108">Vyberte deník plateb pro uložení plateb odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="8eaf8-109">Vyberte deník nebo jej zadejte ručně.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="8eaf8-110">Klikněte na položku Zadat platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="8eaf8-111">Možnost Zadat platby odběratele se používá k záznamu jedné platby odběratele v rámci jedné operace.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="8eaf8-112">Zadáte informace o platbě nahoře a potom označíte faktury, které byly zaplaceny pomocí dané platby, všechny na stejné stránce.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="8eaf8-113">Zadejte odběratele, od kterého jste platbu obdrželi.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="8eaf8-114">Pokud neznáte odběratele, ale víte, která transakce byla zaplacena, můžete platbu zadat s použitím pole Transakce.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="8eaf8-115">Zadejte nebo vyberte fakturu v poli Transakce.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="8eaf8-116">Po výběru transakce se automaticky nastaví výchozí odběratel.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="8eaf8-117">Do pole Platební reference zadejte platební referenci.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="8eaf8-118">Platební referencí může být číslo šeku odběratele nebo reference z elektronické platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="8eaf8-119">Platební reference je vyžadována, pouze pokud vyberete zahrnutí platby na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="8eaf8-120">Vyberte, zda platby mají být zahrnuty na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="8eaf8-121">Zadejte částku platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="8eaf8-122">Pro částku platby se nenastaví výchozí hodnota.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-122">The payment amount will not default.</span></span> <span data-ttu-id="8eaf8-123">Je nutné ji zadat ručně.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="8eaf8-124">Označte faktury, které byly odběratelem zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="8eaf8-125">Pokud platba představuje zálohu, není nutné označit žádné faktury pro vyrovnání.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="8eaf8-126">Platbu lze přesto uložit a zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="8eaf8-127">K vyrovnání faktury může dojít později.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="8eaf8-128">Zadejte částku platby, která má vyrovnána na označené faktuře.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="8eaf8-129">Toto pole lze použít, když je platba určená pro částečnou platbu.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="8eaf8-130">Pokud nezadáte částku, bude částka k vyrovnání určena automaticky.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="8eaf8-131">Klikněte na položku Uložit v deníku.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-131">Click Save in journal.</span></span>
    * <span data-ttu-id="8eaf8-132">Před uložením platby do deníku se ujistěte, že je definován protiúčet.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="8eaf8-133">Když použijete položku Uložit v deníku, platbu tím uložíte a přesunete ji do deníku.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="8eaf8-134">Poté můžete pokračovat v zadávání další platby.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="8eaf8-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-135">Close the page.</span></span>
14. <span data-ttu-id="8eaf8-136">Klikněte na položku Řádky.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-136">Click Lines.</span></span>
    * <span data-ttu-id="8eaf8-137">Při otevírání řádků se zobrazí všechny platby zaznamenané na stránce Zadat platby odběratele a uložené do deníku.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="8eaf8-138">Na této stránce také můžete zadat nové platby odběratele nebo upravit existující platbu odběratele před zaúčtováním.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="8eaf8-139">Klikněte na položku Nová a vytvořte tak další platbu.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="8eaf8-140">Vyberte odběratele, od kterého jste platbu obdrželi.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="8eaf8-141">Pokud neznáte odběratele, ale víte, která faktura byla prostřednictvím této platby uhrazena, můžete fakturu ručně zadat nebo vybrat v poli Faktura.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="8eaf8-142">Po výběru faktury se nastaví výchozí odběratel.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="8eaf8-143">Klikněte na položku Vyrovnat transakce a označte faktury, které byly zaplaceny.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="8eaf8-144">Platba nemusí vyrovnávat žádnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="8eaf8-145">Pokud se jedná o zálohu nebo pokud nevíte, která faktura byla uhrazena, můžete platbu zadat a zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="8eaf8-146">Platbu pak můžete vyrovnat pomocí faktury později.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="8eaf8-147">Označte faktury, které byly platbou uhrazeny.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="8eaf8-148">Zadejte částku platby, která bude na faktuře vyrovnána.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="8eaf8-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-149">Click OK.</span></span>
21. <span data-ttu-id="8eaf8-150">Do pole Platební reference zadejte platební referenci.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="8eaf8-151">.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-151">.</span></span>
    * <span data-ttu-id="8eaf8-152">Platební reference je vyžadována, pouze pokud vyberete zahrnutí platby na vkladové složence.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="8eaf8-153">Zaúčtujte platby odběratele.</span><span class="sxs-lookup"><span data-stu-id="8eaf8-153">Post the customer payments.</span></span> 

