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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 706b245971ba065bae86e31853832f721a6f9aff
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/28/2020
ms.locfileid: "4441368"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="f31a8-103">Přidání nebo kopírování leasingů (Preview)</span><span class="sxs-lookup"><span data-stu-id="f31a8-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f31a8-104">Toto téma vysvětluje, jak vytvořit leasing od začátku v leasingu majetku, a také jak vytvořit leasing kopírováním existujícího leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="f31a8-105">Proces vytváření leasingu od začátku zahrnuje zadání informací o novém leasingu a následné vytvoření plánu leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="f31a8-106">Po vytvoření alespoň jednoho leasingu může být jednodušší zkopírovat informace ze stávajícího leasingu a poté tyto informace upravit podle potřeby k vytvoření nového leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="f31a8-107">Vytvoření leasingu</span><span class="sxs-lookup"><span data-stu-id="f31a8-107">Create a lease</span></span>

<span data-ttu-id="f31a8-108">Pomocí těchto kroků vytvoříte leasing v leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="f31a8-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="f31a8-109">Na stránce **Shrnutí leasingu** v podokně Akce vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="f31a8-110">Zadejte informace o leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-110">Enter the lease information.</span></span> <span data-ttu-id="f31a8-111">Pole, která jsou povinná, mají červené ohraničení.</span><span class="sxs-lookup"><span data-stu-id="f31a8-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="f31a8-112">Vytvoření plánu leasingu</span><span class="sxs-lookup"><span data-stu-id="f31a8-112">Create a lease schedule</span></span>

<span data-ttu-id="f31a8-113">Po dokončení zadávání informací o leasingu postupujte podle těchto kroků a vytvořte plán leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="f31a8-114">Finanční dimenze se mohou změnit na základě libovolných akýchkoli vlastních finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f31a8-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="f31a8-115">Volbou **Vytvořit plány** vygenerujete leasingové knihy.</span><span class="sxs-lookup"><span data-stu-id="f31a8-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="f31a8-116">Leasingové knihy zahrnují splátkové, amortizační, odpisové a výdajové plány.</span><span class="sxs-lookup"><span data-stu-id="f31a8-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="f31a8-117">Chcete-li otevřít leasingové knihy a zobrazit nově vytvořené plány, vyberte kartu **Knihy**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="f31a8-118">Stránka **Podrobnosti o knize** ukazuje, jak je leasing zaúčtován v knihách, které k němu byly přiděleny.</span><span class="sxs-lookup"><span data-stu-id="f31a8-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="f31a8-119">Odtud můžete zobrazit plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="f31a8-120">Harmonogram plateb obsahuje vstupy z karty **Řádky platebního kalendáře** na stránce **Přidání leasingu**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="f31a8-121">Stále můžete změnit každou částku platby a variabilní platbu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="f31a8-122">Leasingový závazek se počítá na základě upraveného platebního kalendáře.</span><span class="sxs-lookup"><span data-stu-id="f31a8-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="f31a8-123">Po dokončení kontroly platebního kalendáře vyberte **Potvrdit kalendář**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="f31a8-124">Po potvrzení kalendáře již není leasing k dispozici pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="f31a8-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f31a8-125">Systém automaticky vypočítá dobu trvání leasingu z řádků platebního kalendáře na stránce **Přidání leasingu**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="f31a8-126">Aby systém vypočítal dobu trvání leasingu v měsících, vyhledá rozdíl mezi počátečním a konečným datem pro konkrétní řádek platebního kalendáře.</span><span class="sxs-lookup"><span data-stu-id="f31a8-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="f31a8-127">Poté se přesune na další řádek platebního kalendáře a znovu vyhledá rozdíl.</span><span class="sxs-lookup"><span data-stu-id="f31a8-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="f31a8-128">Nakonec systém sečte všechny částky k určení doby trvání leasingu v měsících.</span><span class="sxs-lookup"><span data-stu-id="f31a8-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="f31a8-129">Chcete-li zobrazit vypočítané období úrokových výdajů, otevřete stránku **Plán amortizace závazku**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="f31a8-130">Chcete-li zobrazit vypočítané lineární odpisy, otevřete stránku **Plán odpisu majetku**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="f31a8-131">Poté, co dokončíte kontrolu vypočítané částky, můžete vytvořit položku deníku počátečního uznání na stránce **Počáteční uznání**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="f31a8-132">Zobrazí se zpráva, že deník byl vytvořen.</span><span class="sxs-lookup"><span data-stu-id="f31a8-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f31a8-133">Položka deníku se nezaúčtuje do hlavní knihy, dokud ji ručně nezaúčtujete.</span><span class="sxs-lookup"><span data-stu-id="f31a8-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="f31a8-134">Chcete-li zkontrolovat navrhovanou položku počátečního uznání před jejím odesláním, vyberte **Deník leasingu majetku**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f31a8-135">Deník leasingu majetku nelze vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="f31a8-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f31a8-136">Automaticky se vytvoří, když se vytvoří plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="f31a8-137">Až dokončíte kontrolu položky deníku počátečního uznání a jste připraveni ji zaúčtovat, volbou **Zaúčtovat** uznáte používaný majetek a leasingový závazek v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="f31a8-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="f31a8-138">Kopírování leasingu</span><span class="sxs-lookup"><span data-stu-id="f31a8-138">Copy a lease</span></span>

<span data-ttu-id="f31a8-139">Pronájem majetku vám umožňuje zkopírovat podrobnosti leasingu a vytvořit nový leasing, který má stejné informace.</span><span class="sxs-lookup"><span data-stu-id="f31a8-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="f31a8-140">Poté můžete změnit pole leasingu, než vytvoříte plány kopírovaného leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="f31a8-141">Na stránce **Shrnutí leasingu** vyberte leasing, který chcete kopírovat, a poté v podokně akcí vyberte **Kopírovat leasing**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f31a8-142">Pokud je vypnutý parametr **Ručně** pro číselnou sekvenci ID leasingu, další číslo v sekvenci je automaticky generováno jako ID leasingu zkopírovaného leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="f31a8-143">Pokud je zapnutý parametr **Ručně**, zobrazí se zpráva s výzvou k zadání ID leasingu, než budete pokračovat v kopírování leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="f31a8-144">Vyberte **Kopírovat**.</span><span class="sxs-lookup"><span data-stu-id="f31a8-144">Select **Copy**.</span></span> <span data-ttu-id="f31a8-145">Podrobnosti leasingu z vybraného leasingu jsou zkopírovány do nového leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="f31a8-146">Poté můžete upravit podrobnosti nového leasingu, než jej uložíte, a vytvořit plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="f31a8-147">Deník leasingu majetku</span><span class="sxs-lookup"><span data-stu-id="f31a8-147">Asset leasing journal</span></span>

<span data-ttu-id="f31a8-148">Všechny položky deníku, které jsou vytvořeny v leasingu majetku, jsou obsaženy v deníku leasingu majetku.</span><span class="sxs-lookup"><span data-stu-id="f31a8-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="f31a8-149">Na stránce **Deník leasingu majetku** (**Leasing majetku \> Položky deníku \> Deník leasingu majetku**), můžete filtrovat podle stavu zaúčtování, zobrazit konkrétní položky deníku a doklady a zaúčtovat nezaúčtované položky deníku.</span><span class="sxs-lookup"><span data-stu-id="f31a8-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="f31a8-150">Deník leasingu majetku nelze vytvořit ručně.</span><span class="sxs-lookup"><span data-stu-id="f31a8-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f31a8-151">Automaticky se vytvoří, když se vytvoří plány leasingu.</span><span class="sxs-lookup"><span data-stu-id="f31a8-151">It's automatically created when lease schedules are created.</span></span>
