---
title: Definice účtování
description: Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "310247"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="b1397-103">Příklady definice účtování</span><span class="sxs-lookup"><span data-stu-id="b1397-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1397-104">Tento článek obsahuje příklady, které ukazují způsob použití definice zaúčtování břemen nákupních objednávek a přidělení rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b1397-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="b1397-105">než si přečtete obsah tohoto tématu, měli byste se seznámit s účtovacími definicemi a definicemi účtování transakcí.</span><span class="sxs-lookup"><span data-stu-id="b1397-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="b1397-106">Informace naleznete v tématu [Definice účtování](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="b1397-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="b1397-107">Následující příklady lze nastavit na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="b1397-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="b1397-108">Každý příklad obsahuje tyto oddíly:</span><span class="sxs-lookup"><span data-stu-id="b1397-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="b1397-109">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="b1397-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="b1397-110">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="b1397-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="b1397-111">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="b1397-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="b1397-112">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="b1397-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b1397-113">Když dojde ke shodě mezi účty a hodnotami dimenze v podokně **Kritéria shody** pro definici účtování a účty a hodnoty dimenze v transakci, záznamy v hlavní knize jsou generovány na základě podokna **Vytvořené položky** pro definice účtování.</span><span class="sxs-lookup"><span data-stu-id="b1397-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="b1397-114">Pokud chcete přidružit definice účtování ke konkrétnímu typu transakce, použijte stránku **Definice účtování transakcí**.</span><span class="sxs-lookup"><span data-stu-id="b1397-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="b1397-115">Po přidružení definice účtování k typu transakce a výběru možnost **Použít definice účtování** na stránce **Parametry hlavní knihy** musí všechny transakce vybraného typu používat definice účtování.</span><span class="sxs-lookup"><span data-stu-id="b1397-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="b1397-116">Příklad: břemeno nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="b1397-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="b1397-117">Jestliže povolíte zpracování břemene výběrem možnosti **Povolit proces břemena** na stránce **Parametry hlavní knihy**, definice účtování musí být použity pro záznam břemen do hlavní knihy pro všechny účty, které budou rezervovány.</span><span class="sxs-lookup"><span data-stu-id="b1397-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="b1397-118">Ve většině případů jsou rezervovány všechny účty nákladů v rozvaze.</span><span class="sxs-lookup"><span data-stu-id="b1397-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="b1397-119">Definice účtování pro břemena jsou nastaveny pro modul **Nakupování** na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="b1397-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b1397-120">Poté v oblasti **Nakupování** na stránce **Definice účtování transakcí** můžete vybrat typ transakce **Nákupní objednávka** a přiřadit tak definici účtování k nákupní objednávce.</span><span class="sxs-lookup"><span data-stu-id="b1397-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="b1397-121">Všechny transakce dokladu pro břemeno nákupní objednávky musí mít zůstatek (debet se musí rovnat kreditům) v každé jedinečné dimenzi na dokladu.</span><span class="sxs-lookup"><span data-stu-id="b1397-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b1397-122">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="b1397-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b1397-123">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-123">Account structure</span></span>       | <span data-ttu-id="b1397-124">Číslo účtu shody</span><span class="sxs-lookup"><span data-stu-id="b1397-124">Match account number</span></span> | <span data-ttu-id="b1397-125">Priorita </span><span class="sxs-lookup"><span data-stu-id="b1397-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b1397-126">Účetní struktura – zisky a ztráty</span><span class="sxs-lookup"><span data-stu-id="b1397-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b1397-127">1</span><span class="sxs-lookup"><span data-stu-id="b1397-127">1</span></span>        |

<span data-ttu-id="b1397-128"><em>Prázdná hodnota v poli \**Číslo účtu shody</em>* znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.</span><span class="sxs-lookup"><span data-stu-id="b1397-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b1397-129">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="b1397-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b1397-130">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-130">Account structure</span></span> | <span data-ttu-id="b1397-131">Generované číslo účtu</span><span class="sxs-lookup"><span data-stu-id="b1397-131">Generated account number</span></span>                    | <span data-ttu-id="b1397-132">Generované hodnoty Má dáti/Dal</span><span class="sxs-lookup"><span data-stu-id="b1397-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="b1397-133">Zůstatek</span><span class="sxs-lookup"><span data-stu-id="b1397-133">Balance</span></span>           | <span data-ttu-id="b1397-134">300143 - -(účet pro břemeno)</span><span class="sxs-lookup"><span data-stu-id="b1397-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="b1397-135">Stejné</span><span class="sxs-lookup"><span data-stu-id="b1397-135">Same</span></span>                   |
| <span data-ttu-id="b1397-136">Zůstatek</span><span class="sxs-lookup"><span data-stu-id="b1397-136">Balance</span></span>           | <span data-ttu-id="b1397-137">300144 - -(rezerva pro účet pro břemeno)</span><span class="sxs-lookup"><span data-stu-id="b1397-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="b1397-138">Vyvažující</span><span class="sxs-lookup"><span data-stu-id="b1397-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b1397-139">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="b1397-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b1397-140">Hodnoty pro účty a dimenze pochází z rozúčtování zadaného pro řádek nákupní objednávky nebo z účtů a dimenzí, které jsou generovány automaticky na základě výchozího nastavení pro dodavatele, položky, kategorie a šablony dimenze.</span><span class="sxs-lookup"><span data-stu-id="b1397-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="b1397-141">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="b1397-141">Account + dimensions</span></span>           | <span data-ttu-id="b1397-142">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="b1397-142">Debit</span></span>  | <span data-ttu-id="b1397-143">Kreditní</span><span class="sxs-lookup"><span data-stu-id="b1397-143">Credit</span></span> | <span data-ttu-id="b1397-144">Komentář</span><span class="sxs-lookup"><span data-stu-id="b1397-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b1397-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b1397-146">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b1397-147">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="b1397-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b1397-148">Generované položky hlavní knihy se vytvářejí pro záznam břemen.</span><span class="sxs-lookup"><span data-stu-id="b1397-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="b1397-149">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="b1397-149">Account + dimensions</span></span>           | <span data-ttu-id="b1397-150">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="b1397-150">Debit</span></span>  | <span data-ttu-id="b1397-151">Kreditní</span><span class="sxs-lookup"><span data-stu-id="b1397-151">Credit</span></span> | <span data-ttu-id="b1397-152">Komentář</span><span class="sxs-lookup"><span data-stu-id="b1397-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b1397-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b1397-154">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-154">250.00</span></span> |        |         |
| <span data-ttu-id="b1397-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b1397-156">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-156">250.00</span></span> |         |

<span data-ttu-id="b1397-157">V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování.</span><span class="sxs-lookup"><span data-stu-id="b1397-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b1397-158">Z toho vyplývá, při vyhodnocení 606500-OU\_1-OU\_3566-Training jsou generované položky vytvořeny pro účty, které jsou definovány v podokně **Generované položky** pro definici účtování.</span><span class="sxs-lookup"><span data-stu-id="b1397-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="b1397-159">Příklad: rozdělení rozpočtu</span><span class="sxs-lookup"><span data-stu-id="b1397-159">Example: Budget appropriations</span></span>
<span data-ttu-id="b1397-160">Když povolíte rozdělení rozpočtu výběrem možnosti **Povolit rozdělení rozpočtu** na stránce **Parametry hlavní knihy**, je nutné použít definice účtování pro záznam položek registru rozpočtu do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b1397-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="b1397-161">Když je konfigurace kontroly rozpočtu aktivní a zapnutá, definice účtování a definice účtování transakcí lze použít k podpoře záznamu položek pro odhady, revize, převody, projekty, dlouhodobý majetek a prognózy nabídky a poptávky v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="b1397-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="b1397-162">Pro nastavení definice účtování pro položky registru rozpočtu s typem rozpočtu **Původní rozpočet**, když není povoleno rozdělení příjmů, vyberte modul **Rozpočet** na stránce **Definice účtování**.</span><span class="sxs-lookup"><span data-stu-id="b1397-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="b1397-163">Potom můžete v oblasti **Rozpočet** na stránce **Definice účtování transakcí** použít kódy rozpočtu a přidružit tak definice účtování k položkám registru rozpočtu, které mají typ rozpočtu **Původní rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="b1397-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="b1397-164">Pokud jsou povoleny rozdělení příjmů rozpočtu a definice účtování, položky registru rozpočtu jsou zaznamenány pro kontrolu rozpočtu v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="b1397-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="b1397-165">Definice účtování – kritéria shody</span><span class="sxs-lookup"><span data-stu-id="b1397-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="b1397-166">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-166">Account structure</span></span>       | <span data-ttu-id="b1397-167">Číslo účtu shody</span><span class="sxs-lookup"><span data-stu-id="b1397-167">Match account number</span></span> | <span data-ttu-id="b1397-168">Priorita </span><span class="sxs-lookup"><span data-stu-id="b1397-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="b1397-169">Účetní struktura – zisky a ztráty</span><span class="sxs-lookup"><span data-stu-id="b1397-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="b1397-170">1</span><span class="sxs-lookup"><span data-stu-id="b1397-170">1</span></span>        |

<span data-ttu-id="b1397-171"><em>Prázdná hodnota v poli \**Číslo účtu shody</em>* znamená, že všechny odpovídající účty v definované účetní struktuře jsou součástí pravidel párování.</span><span class="sxs-lookup"><span data-stu-id="b1397-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="b1397-172">Definice účtování – generované položky</span><span class="sxs-lookup"><span data-stu-id="b1397-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="b1397-173">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-173">Account structure</span></span> | <span data-ttu-id="b1397-174">Generované číslo účtu</span><span class="sxs-lookup"><span data-stu-id="b1397-174">Generated account number</span></span>              | <span data-ttu-id="b1397-175">Generované hodnoty Má dáti/Dal</span><span class="sxs-lookup"><span data-stu-id="b1397-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="b1397-176">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-176">Account structure</span></span> | <span data-ttu-id="b1397-177">300145 - -(účet pro odhadované výnosy)</span><span class="sxs-lookup"><span data-stu-id="b1397-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="b1397-178">Stejné</span><span class="sxs-lookup"><span data-stu-id="b1397-178">Same</span></span>                   |
| <span data-ttu-id="b1397-179">Účetní struktura</span><span class="sxs-lookup"><span data-stu-id="b1397-179">Account structure</span></span> | <span data-ttu-id="b1397-180">300146 - -(účet pro rozdělení)</span><span class="sxs-lookup"><span data-stu-id="b1397-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="b1397-181">Vyvažující</span><span class="sxs-lookup"><span data-stu-id="b1397-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="b1397-182">Transakce s účty, hodnoty dimenzí a částky</span><span class="sxs-lookup"><span data-stu-id="b1397-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="b1397-183">Účty, hodnoty dimenzí a částky pro účetní položku rozpočtu zadáváte na stránce **Položka registru rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="b1397-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="b1397-184">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="b1397-184">Account + dimensions</span></span>           | <span data-ttu-id="b1397-185">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="b1397-185">Debit</span></span> | <span data-ttu-id="b1397-186">Kreditní</span><span class="sxs-lookup"><span data-stu-id="b1397-186">Credit</span></span> | <span data-ttu-id="b1397-187">Komentář</span><span class="sxs-lookup"><span data-stu-id="b1397-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="b1397-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="b1397-189">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="b1397-190">Položky hlavní knihy generované z definice účtování</span><span class="sxs-lookup"><span data-stu-id="b1397-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="b1397-191">Generované položky v hlavní knize se vytvoří pro záznam původního rozpočtu v jednotlivých dimenzích.</span><span class="sxs-lookup"><span data-stu-id="b1397-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="b1397-192">Účet + dimenze</span><span class="sxs-lookup"><span data-stu-id="b1397-192">Account + dimensions</span></span>           | <span data-ttu-id="b1397-193">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="b1397-193">Debit</span></span>  | <span data-ttu-id="b1397-194">Kreditní</span><span class="sxs-lookup"><span data-stu-id="b1397-194">Credit</span></span> | <span data-ttu-id="b1397-195">Komentář</span><span class="sxs-lookup"><span data-stu-id="b1397-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="b1397-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="b1397-197">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-197">250.00</span></span> |         |
| <span data-ttu-id="b1397-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="b1397-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="b1397-199">250.00</span><span class="sxs-lookup"><span data-stu-id="b1397-199">250.00</span></span> |        |         |

<span data-ttu-id="b1397-200">V tomto příkladu je jakékoli účet součástí účetní struktury – zisky a ztráty odpovídají kritériím definice účtování.</span><span class="sxs-lookup"><span data-stu-id="b1397-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="b1397-201">Z toho vyplývá při vyhodnocení 606400-OU\_1-OU\_3566-Training se vytvoří generované položky hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b1397-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





