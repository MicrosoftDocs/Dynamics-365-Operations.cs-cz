---
title: Přidání nebo kopírování leasingů (Preview)
description: Toto téma popisuje, jak vytvořit nový leasing zadáním informací o něm do leasingu majetku nebo zkopírováním informací z existujícího leasingu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: abbf04d009a4b347792cd8b317e334da2a4cbbee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969596"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="b1b49-103">Přidání nebo kopírování leasingů (Preview)</span><span class="sxs-lookup"><span data-stu-id="b1b49-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1b49-104">Toto téma vysvětluje, jak vytvořit leasing od začátku v leasingu majetku, a také jak vytvořit leasing kopírováním existujícího leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="b1b49-105">Proces vytváření leasingu od začátku zahrnuje zadání informací o novém leasingu a následné vytvoření plánu leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="b1b49-106">Po vytvoření alespoň jednoho leasingu může být jednodušší zkopírovat informace ze stávajícího leasingu a poté tyto informace upravit podle potřeby k vytvoření nového leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="b1b49-107">Vytvoření leasingu</span><span class="sxs-lookup"><span data-stu-id="b1b49-107">Create a lease</span></span>

<span data-ttu-id="b1b49-108">Pomocí těchto kroků vytvoříte leasing v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="b1b49-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="b1b49-109">Na stránce **Shrnutí leasingu** v podokně Akce vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="b1b49-110">Zadejte informace o leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-110">Enter the lease information.</span></span> <span data-ttu-id="b1b49-111">Pole, která jsou povinná, mají červené ohraničení.</span><span class="sxs-lookup"><span data-stu-id="b1b49-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="b1b49-112">Vytvoření plánu leasingu</span><span class="sxs-lookup"><span data-stu-id="b1b49-112">Create a lease schedule</span></span>

<span data-ttu-id="b1b49-113">Po dokončení zadávání informací o leasingu postupujte podle těchto kroků a vytvořte plán leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="b1b49-114">Finanční dimenze se mohou změnit na základě libovolných akýchkoli vlastních finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="b1b49-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="b1b49-115">Volbou **Vytvořit plány** vygenerujete leasingové knihy.</span><span class="sxs-lookup"><span data-stu-id="b1b49-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="b1b49-116">Leasingové knihy zahrnují splátkové, amortizační, odpisové a výdajové plány.</span><span class="sxs-lookup"><span data-stu-id="b1b49-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="b1b49-117">Chcete-li otevřít leasingové knihy a zobrazit nově vytvořené plány, vyberte kartu **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="b1b49-118">Stránka **Podrobnosti o knize** ukazuje, jak je leasing zaúčtován v knihách, které k němu byly přiděleny.</span><span class="sxs-lookup"><span data-stu-id="b1b49-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="b1b49-119">Odtud můžete zobrazit plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="b1b49-120">Harmonogram plateb obsahuje vstupy z karty **Řádky platebního kalendáře** na stránce **Přidání leasingu**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="b1b49-121">Stále můžete změnit každou částku platby a variabilní platbu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="b1b49-122">Leasingový závazek se počítá na základě upraveného platebního kalendáře.</span><span class="sxs-lookup"><span data-stu-id="b1b49-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="b1b49-123">Po dokončení kontroly platebního kalendáře vyberte **Potvrdit kalendář**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="b1b49-124">Po potvrzení kalendáře již není leasing k dispozici pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="b1b49-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1b49-125">Systém automaticky vypočítá dobu trvání leasingu z řádků platebního kalendáře na stránce **Přidání leasingu**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="b1b49-126">Aby systém vypočítal dobu trvání leasingu v měsících, vyhledá rozdíl mezi počátečním a konečným datem pro konkrétní řádek platebního kalendáře.</span><span class="sxs-lookup"><span data-stu-id="b1b49-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="b1b49-127">Poté se přesune na další řádek platebního kalendáře a znovu vyhledá rozdíl.</span><span class="sxs-lookup"><span data-stu-id="b1b49-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="b1b49-128">Nakonec systém sečte všechny částky k určení doby trvání leasingu v měsících.</span><span class="sxs-lookup"><span data-stu-id="b1b49-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="b1b49-129">Chcete-li zobrazit vypočítané období úrokových výdajů, otevřete stránku **Plán amortizace závazku**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="b1b49-130">Chcete-li zobrazit vypočítané lineární odpisy, otevřete stránku **Plán odpisu majetku**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="b1b49-131">Poté, co dokončíte kontrolu vypočítané částky, můžete vytvořit položku deníku počátečního uznání na stránce **Počáteční uznání**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="b1b49-132">Zobrazí se zpráva, že deník byl vytvořen.</span><span class="sxs-lookup"><span data-stu-id="b1b49-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1b49-133">Položka deníku se nezaúčtuje do hlavní knihy, dokud ji ručně nezaúčtujete.</span><span class="sxs-lookup"><span data-stu-id="b1b49-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="b1b49-134">Chcete-li zkontrolovat navrhovanou položku počátečního uznání před jejím odesláním, vyberte **Deník leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1b49-135">Deník leasingu majetku nelze vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="b1b49-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="b1b49-136">Automaticky se vytvoří, když se vytvoří plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="b1b49-137">Až dokončíte kontrolu položky deníku počátečního uznání a jste připraveni ji zaúčtovat, volbou **Zaúčtovat** uznáte používaný majetek a leasingový závazek v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="b1b49-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="b1b49-138">Kopírování leasingu</span><span class="sxs-lookup"><span data-stu-id="b1b49-138">Copy a lease</span></span>

<span data-ttu-id="b1b49-139">Pronájem majetku vám umožňuje zkopírovat podrobnosti leasingu a vytvořit nový leasing, který má stejné informace.</span><span class="sxs-lookup"><span data-stu-id="b1b49-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="b1b49-140">Poté můžete změnit pole leasingu, než vytvoříte plány kopírovaného leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="b1b49-141">Na stránce **Shrnutí leasingu** vyberte leasing, který chcete kopírovat, a poté v podokně akcí vyberte **Kopírovat leasing**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1b49-142">Pokud je vypnutý parametr **Ručně** pro číselnou sekvenci ID leasingu, další číslo v sekvenci je automaticky generováno jako ID leasingu zkopírovaného leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="b1b49-143">Pokud je zapnutý parametr **Ručně**, zobrazí se zpráva s výzvou k zadání ID leasingu, než budete pokračovat v kopírování leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="b1b49-144">Vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="b1b49-144">Select **Copy**.</span></span> <span data-ttu-id="b1b49-145">Podrobnosti leasingu z vybraného leasingu jsou zkopírovány do nového leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="b1b49-146">Poté můžete upravit podrobnosti nového leasingu, než jej uložíte, a vytvořit plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="b1b49-147">Deník leasingu majetku</span><span class="sxs-lookup"><span data-stu-id="b1b49-147">Asset leasing journal</span></span>

<span data-ttu-id="b1b49-148">Všechny položky deníku, které jsou vytvořeny v leasingu majetku, jsou obsaženy v deníku leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="b1b49-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="b1b49-149">Na stránce **Deník leasingu majetku** (**Leasing majetku \> Položky deníku \> Deník leasingu majetku**), můžete filtrovat podle stavu zaúčtování, zobrazit konkrétní položky deníku a doklady a zaúčtovat nezaúčtované položky deníku.</span><span class="sxs-lookup"><span data-stu-id="b1b49-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="b1b49-150">Deník leasingu majetku nelze vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="b1b49-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="b1b49-151">Automaticky se vytvoří, když se vytvoří plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="b1b49-151">It's automatically created when lease schedules are created.</span></span>
