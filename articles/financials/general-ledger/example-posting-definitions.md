---
title: "Definice účtování"
description: "Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 004f3f24ec410d9f0e7d1e7264ec2730b9467410
ms.contentlocale: cs-cz
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definition-examples"></a><span data-ttu-id="1ff58-103">Příklady definice účtování</span><span class="sxs-lookup"><span data-stu-id="1ff58-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1ff58-104">Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="1ff58-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="1ff58-105">než si přečtete obsah tohoto tématu, měli byste se seznámit s účtovacími definicemi a definicemi účtování transakcí.</span><span class="sxs-lookup"><span data-stu-id="1ff58-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="1ff58-106">Informace naleznete v tématu [Definice účtování](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="1ff58-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="1ff58-107">Následující příklady lze nastavit na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="1ff58-108">Každý příklad obsahuje tyto oddíly:</span><span class="sxs-lookup"><span data-stu-id="1ff58-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="1ff58-109">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="1ff58-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="1ff58-110">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="1ff58-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="1ff58-111">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="1ff58-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="1ff58-112">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="1ff58-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="1ff58-113">Když dojde ke shodě mezi účty a hodnotami dimenze v podokně **Kritéria shody** pro definici účtování a účty a hodnoty dimenze v transakci, záznamy v hlavní knize jsou generovány na základě podokna **Vytvořené položky** pro definice účtování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="1ff58-114">Pokud chcete přidružit definice účtování ke konkrétnímu typu transakce, použijte stránku **Definice účtování transakcí**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="1ff58-115">Po přidružení definice účtování k typu transakce a výběru možnost **Použít definice účtování** na stránce **Parametry hlavní knihy** musí všechny transakce vybraného typu používat definice účtování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="1ff58-116">Příklad: břemeno nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="1ff58-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="1ff58-117">Jestliže povolíte zpracování břemene výběrem možnosti **Povolit proces břemena** na stránce **Parametry hlavní knihy**, definice účtování musí být použity pro záznam břemen do hlavní knihy pro všechny účty, které budou rezervovány.</span><span class="sxs-lookup"><span data-stu-id="1ff58-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="1ff58-118">Ve většině případů jsou rezervovány všechny účty nákladů v rozvaze.</span><span class="sxs-lookup"><span data-stu-id="1ff58-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="1ff58-119">Definice účtování pro břemena jsou nastaveny pro modul **Nakupování** na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="1ff58-120">Poté v oblasti **Nakupování** na stránce **Definice účtování transakcí** můžete vybrat typ transakce **Nákupní objednávka** a přiřadit tak definici účtování k nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="1ff58-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="1ff58-121">Všechny transakce dokladu pro břemeno nákupní objednávky musí mít zůstatek (debet se musí rovnat kreditům) v každé jedinečné dimenzi na dokladu.</span><span class="sxs-lookup"><span data-stu-id="1ff58-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="1ff58-122">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="1ff58-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="1ff58-123">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-123">Account structure</span></span>       | <span data-ttu-id="1ff58-124">Číslo účtu shody</span><span class="sxs-lookup"><span data-stu-id="1ff58-124">Match account number</span></span> | <span data-ttu-id="1ff58-125">Priorita</span><span class="sxs-lookup"><span data-stu-id="1ff58-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="1ff58-126">Účetní struktura – zisky a ztráty</span><span class="sxs-lookup"><span data-stu-id="1ff58-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="1ff58-127">1</span><span class="sxs-lookup"><span data-stu-id="1ff58-127">1</span></span>        |

<span data-ttu-id="1ff58-128">* Prázdná hodnota v poli **Číslo účtu shody** znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="1ff58-129">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="1ff58-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="1ff58-130">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-130">Account structure</span></span> | <span data-ttu-id="1ff58-131">Generované číslo účtu</span><span class="sxs-lookup"><span data-stu-id="1ff58-131">Generated account number</span></span>                    | <span data-ttu-id="1ff58-132">Generované hodnoty Má dáti/Dal</span><span class="sxs-lookup"><span data-stu-id="1ff58-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="1ff58-133">Zůstatek</span><span class="sxs-lookup"><span data-stu-id="1ff58-133">Balance</span></span>           | <span data-ttu-id="1ff58-134">300143 - -(účet pro břemeno)</span><span class="sxs-lookup"><span data-stu-id="1ff58-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="1ff58-135">Stejné</span><span class="sxs-lookup"><span data-stu-id="1ff58-135">Same</span></span>                   |
| <span data-ttu-id="1ff58-136">Zůstatek</span><span class="sxs-lookup"><span data-stu-id="1ff58-136">Balance</span></span>           | <span data-ttu-id="1ff58-137">300144 - -(rezerva pro účet pro břemeno)</span><span class="sxs-lookup"><span data-stu-id="1ff58-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="1ff58-138">Vyvažující</span><span class="sxs-lookup"><span data-stu-id="1ff58-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="1ff58-139">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="1ff58-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="1ff58-140">Hodnoty pro účty a dimenze pochází z rozúčtování zadaného pro řádek nákupní objednávky nebo z účtů a dimenzí, které jsou generovány automaticky na základě výchozího nastavení pro dodavatele, položky, kategorie a šablony dimenze.</span><span class="sxs-lookup"><span data-stu-id="1ff58-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="1ff58-141">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="1ff58-141">Account + dimensions</span></span>           | <span data-ttu-id="1ff58-142">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="1ff58-142">Debit</span></span>  | <span data-ttu-id="1ff58-143">Kreditní</span><span class="sxs-lookup"><span data-stu-id="1ff58-143">Credit</span></span> | <span data-ttu-id="1ff58-144">Komentář</span><span class="sxs-lookup"><span data-stu-id="1ff58-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="1ff58-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="1ff58-146">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="1ff58-147">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="1ff58-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="1ff58-148">Generované položky hlavní knihy se vytvářejí pro záznam břemen.</span><span class="sxs-lookup"><span data-stu-id="1ff58-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="1ff58-149">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="1ff58-149">Account + dimensions</span></span>           | <span data-ttu-id="1ff58-150">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="1ff58-150">Debit</span></span>  | <span data-ttu-id="1ff58-151">Kreditní</span><span class="sxs-lookup"><span data-stu-id="1ff58-151">Credit</span></span> | <span data-ttu-id="1ff58-152">Komentář</span><span class="sxs-lookup"><span data-stu-id="1ff58-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="1ff58-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="1ff58-154">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-154">250.00</span></span> |        |         |
| <span data-ttu-id="1ff58-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="1ff58-156">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-156">250.00</span></span> |         |

<span data-ttu-id="1ff58-157">V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="1ff58-158">Z toho vyplývá, při vyhodnocení 606500-OU\_1-OU\_3566-Training jsou generované položky vytvořeny pro účty, které jsou definovány v podokně **Generované položky** pro definici účtování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="1ff58-159">Příklad: rozdělení rozpočtu</span><span class="sxs-lookup"><span data-stu-id="1ff58-159">Example: Budget appropriations</span></span>
<span data-ttu-id="1ff58-160">Když povolíte rozdělení rozpočtu výběrem možnosti **Povolit rozdělení rozpočtu** na stránce **Parametry hlavní knihy**, je nutné použít definice účtování pro záznam položek registru rozpočtu do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1ff58-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="1ff58-161">Když je konfigurace kontroly rozpočtu aktivní a zapnutá, definice účtování a definice účtování transakcí lze použít k podpoře záznamu položek pro odhady, revize, převody, projekty, dlouhodobý majetek a prognózy nabídky a poptávky v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="1ff58-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="1ff58-162">Pro nastavení definice účtování pro položky registru rozpočtu s typem rozpočtu **Původní rozpočet**, když není povoleno rozdělení příjmů, vyberte modul **Rozpočet** na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="1ff58-163">Potom můžete v oblasti **Rozpočet** na stránce **Definice účtování transakcí** použít kódy rozpočtu a přidružit tak definice účtování k položkám registru rozpočtu, které mají typ rozpočtu **Původní rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="1ff58-164">Pokud jsou povoleny rozdělení příjmů rozpočtu a definice účtování, položky registru rozpočtu jsou zaznamenány pro kontrolu rozpočtu v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="1ff58-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="1ff58-165">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="1ff58-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="1ff58-166">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-166">Account structure</span></span>       | <span data-ttu-id="1ff58-167">Číslo účtu shody</span><span class="sxs-lookup"><span data-stu-id="1ff58-167">Match account number</span></span> | <span data-ttu-id="1ff58-168">Priorita</span><span class="sxs-lookup"><span data-stu-id="1ff58-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="1ff58-169">Účetní struktura – zisky a ztráty</span><span class="sxs-lookup"><span data-stu-id="1ff58-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="1ff58-170">1</span><span class="sxs-lookup"><span data-stu-id="1ff58-170">1</span></span>        |

<span data-ttu-id="1ff58-171">* Prázdná hodnota v poli **Číslo účtu shody** znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="1ff58-172">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="1ff58-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="1ff58-173">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-173">Account structure</span></span> | <span data-ttu-id="1ff58-174">Generované číslo účtu</span><span class="sxs-lookup"><span data-stu-id="1ff58-174">Generated account number</span></span>              | <span data-ttu-id="1ff58-175">Generované hodnoty Má dáti/Dal</span><span class="sxs-lookup"><span data-stu-id="1ff58-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="1ff58-176">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-176">Account structure</span></span> | <span data-ttu-id="1ff58-177">300145 - -(účet pro odhadované výnosy)</span><span class="sxs-lookup"><span data-stu-id="1ff58-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="1ff58-178">Stejné</span><span class="sxs-lookup"><span data-stu-id="1ff58-178">Same</span></span>                   |
| <span data-ttu-id="1ff58-179">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="1ff58-179">Account structure</span></span> | <span data-ttu-id="1ff58-180">300146 - -(účet pro rozdělení)</span><span class="sxs-lookup"><span data-stu-id="1ff58-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="1ff58-181">Vyvažující</span><span class="sxs-lookup"><span data-stu-id="1ff58-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="1ff58-182">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="1ff58-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="1ff58-183">Účty, hodnoty dimenzí a částky pro účetní položku rozpočtu zadáváte na stránce **Položka registru rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="1ff58-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="1ff58-184">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="1ff58-184">Account + dimensions</span></span>           | <span data-ttu-id="1ff58-185">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="1ff58-185">Debit</span></span> | <span data-ttu-id="1ff58-186">Kreditní</span><span class="sxs-lookup"><span data-stu-id="1ff58-186">Credit</span></span> | <span data-ttu-id="1ff58-187">Komentář</span><span class="sxs-lookup"><span data-stu-id="1ff58-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="1ff58-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="1ff58-189">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="1ff58-190">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="1ff58-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="1ff58-191">Generované položky v hlavní knize se vytvoří pro záznam původního rozpočtu v jednotlivých dimenzích.</span><span class="sxs-lookup"><span data-stu-id="1ff58-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="1ff58-192">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="1ff58-192">Account + dimensions</span></span>           | <span data-ttu-id="1ff58-193">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="1ff58-193">Debit</span></span>  | <span data-ttu-id="1ff58-194">Kreditní</span><span class="sxs-lookup"><span data-stu-id="1ff58-194">Credit</span></span> | <span data-ttu-id="1ff58-195">Komentář</span><span class="sxs-lookup"><span data-stu-id="1ff58-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="1ff58-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="1ff58-197">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-197">250.00</span></span> |         |
| <span data-ttu-id="1ff58-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="1ff58-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="1ff58-199">250.00</span><span class="sxs-lookup"><span data-stu-id="1ff58-199">250.00</span></span> |        |         |

<span data-ttu-id="1ff58-200">V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování.</span><span class="sxs-lookup"><span data-stu-id="1ff58-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="1ff58-201">Z toho vyplývá při vyhodnocení 606400-OU\_1-OU\_3566-Training se vytvoří generované položky hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="1ff58-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






