---
title: "Číselné řady"
description: "Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 13b47d755a122199608ece386f4f764ee580b2ed
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="number-sequences"></a><span data-ttu-id="15479-103">Číselné řady</span><span class="sxs-lookup"><span data-stu-id="15479-103">Number sequences</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15479-104">Číselné řady v aplikaci slouží ke generování čitelných, jedinečných identifikátorů pro hlavní datové záznamy a záznamy transakcí, které požadují identifikátory.</span><span class="sxs-lookup"><span data-stu-id="15479-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="15479-105">Hlavní záznam dat nebo záznam transakce, která vyžaduje identifikátor, je označován jako *odkaz*.</span><span class="sxs-lookup"><span data-stu-id="15479-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="15479-106">Než bude možné vytvořit nové záznamy pro odkaz, musíte nastavit číselné řady a spojit je s odkazem.</span><span class="sxs-lookup"><span data-stu-id="15479-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="15479-107">Doporučujeme použít k nastavení číselné řady stránky v modulu **Správa organizace**.</span><span class="sxs-lookup"><span data-stu-id="15479-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="15479-108">Jestliže jsou požadována nastavení modulu, můžete k určení číselných řad pro odkaz v daném modulu použít stránku s parametry v modulu.</span><span class="sxs-lookup"><span data-stu-id="15479-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="15479-109">Například na stránce **Pohledávky** a na stránce **Závazky** můžete nastavit skupiny číselných řad pro přidělení konkrétních číselných řad ke konkrétním odběratelům nebo dodavatelům.</span><span class="sxs-lookup"><span data-stu-id="15479-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="15479-110">Pokud jste nastavili číselnou řadu, musíte zadat obor definující, kterou organizace používá číselná řada.</span><span class="sxs-lookup"><span data-stu-id="15479-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="15479-111">Rozsah může být **Sdílený**, **Společnost**, **Právnická osoba** nebo **Provozní jednotka**.</span><span class="sxs-lookup"><span data-stu-id="15479-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="15479-112">Rozsahy **Právnická osoba** a **Společnost** lze kombinovat s nastavením **Fiskální kalendářní období** a vytvořit tak ještě konkrétnější číselné řady.</span><span class="sxs-lookup"><span data-stu-id="15479-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="15479-113">Formáty číselné řady se skládají ze segmentů.</span><span class="sxs-lookup"><span data-stu-id="15479-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="15479-114">Číselné řady s rozsahem jiným než **Sdílený** mohou obsahovat segmenty, které odpovídají jejich rozsahu.</span><span class="sxs-lookup"><span data-stu-id="15479-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="15479-115">Například číselná řada s rozsahem **Právnická osoba** může obsahovat segment právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="15479-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="15479-116">Zahrnutím rozsahu segmentu ve formátu číselné řady lze identifikovat rozsah určitého záznam zobrazením jeho čísla.</span><span class="sxs-lookup"><span data-stu-id="15479-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="15479-117">Kromě segmentů, které odpovídají rozsahům, mohou formáty číselných řad obsahovat segmenty **Konstanta** a **Alfanumerické**.</span><span class="sxs-lookup"><span data-stu-id="15479-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="15479-118">Segment **Konstanta** obsahuje sadu písmen, číslic a symbolů, které se nemění.</span><span class="sxs-lookup"><span data-stu-id="15479-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="15479-119">Segment **Alfanumerické** obsahuje sadu písmen nebo čísel, které narůstají pokaždé, když se číslo použije.</span><span class="sxs-lookup"><span data-stu-id="15479-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="15479-120">Použijte číselný znak (\#) ke znázornění rostoucích čísel a znak ampersand (&) k označení rostoucích písmen.</span><span class="sxs-lookup"><span data-stu-id="15479-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="15479-121">Formát \#\#\#\#\#\_2017 například vytvoří řadu 00001\_2017, 00002\_2017 atd.</span><span class="sxs-lookup"><span data-stu-id="15479-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="15479-122">Příklady číselné řady</span><span class="sxs-lookup"><span data-stu-id="15479-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="15479-123">Následující příklady ukazují, jak segmenty slouží k vytváření formátů číselné řady.</span><span class="sxs-lookup"><span data-stu-id="15479-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="15479-124">Konkrétně příklady znázorňují dopad používání segmentů rozsahu.</span><span class="sxs-lookup"><span data-stu-id="15479-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="15479-125">Čísla vyúčtování výdajů</span><span class="sxs-lookup"><span data-stu-id="15479-125">Expense report numbers</span></span>

<span data-ttu-id="15479-126">V následujícím příkladu čísla sestavy výdajů jsou přiřazeny k právnické osobě s názvem **CS**.</span><span class="sxs-lookup"><span data-stu-id="15479-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="15479-127">**Oblast:** Cestování a výdaje</span><span class="sxs-lookup"><span data-stu-id="15479-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="15479-128">**Odkaz:** Číslo vyúčtování výdajů</span><span class="sxs-lookup"><span data-stu-id="15479-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="15479-129">**Rozsah:** Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="15479-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="15479-130">**Právnická osoba:** CS</span><span class="sxs-lookup"><span data-stu-id="15479-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="15479-131">Segmenty</span><span class="sxs-lookup"><span data-stu-id="15479-131">Segments</span></span>  | <span data-ttu-id="15479-132">Typ segmentu</span><span class="sxs-lookup"><span data-stu-id="15479-132">Segment type</span></span> | <span data-ttu-id="15479-133">Hodnota</span><span class="sxs-lookup"><span data-stu-id="15479-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="15479-134">Segment 1</span><span class="sxs-lookup"><span data-stu-id="15479-134">Segment 1</span></span> | <span data-ttu-id="15479-135">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="15479-135">Legal entity</span></span> | <span data-ttu-id="15479-136">CS</span><span class="sxs-lookup"><span data-stu-id="15479-136">CS</span></span>        |
| <span data-ttu-id="15479-137">Segment 2</span><span class="sxs-lookup"><span data-stu-id="15479-137">Segment 2</span></span> | <span data-ttu-id="15479-138">Konstanta</span><span class="sxs-lookup"><span data-stu-id="15479-138">Constant</span></span>     | <span data-ttu-id="15479-139">-VýDAJ-</span><span class="sxs-lookup"><span data-stu-id="15479-139">-EXPENSE-</span></span> |
| <span data-ttu-id="15479-140">Segment 3</span><span class="sxs-lookup"><span data-stu-id="15479-140">Segment 3</span></span> | <span data-ttu-id="15479-141">Alfanumerické</span><span class="sxs-lookup"><span data-stu-id="15479-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="15479-142">**Příklad formátovaného čísla**: CS-VÝDAJ-0039</span><span class="sxs-lookup"><span data-stu-id="15479-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="15479-143">Můžete nastavit podobný formát číselné řady pro ostatní právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="15479-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="15479-144">Například u právnické osoby, která se nazývá **RW**, pokud změníte pouze hodnotu segmentu právnické osoby, formátované číslo bude RW-VÝDAJ-0039.</span><span class="sxs-lookup"><span data-stu-id="15479-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="15479-145">Můžete také změnit celý formát číselné řady pro ostatní právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="15479-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="15479-146">Například můžete vynechat rozsah segmentu právnické osoby k vytvoření formátovaného čísla, jako je Výd-0001.</span><span class="sxs-lookup"><span data-stu-id="15479-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="15479-147">Čísla prodejních objednávek</span><span class="sxs-lookup"><span data-stu-id="15479-147">Sales order numbers</span></span>

<span data-ttu-id="15479-148">V následujícím příkladu čísla prodejních objednávek jsou přiřazena k ID společnosti **CEU**.</span><span class="sxs-lookup"><span data-stu-id="15479-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="15479-149">**Oblast:** Prodej</span><span class="sxs-lookup"><span data-stu-id="15479-149">**Area:** Sales</span></span> 
- <span data-ttu-id="15479-150">**Odkaz:** Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="15479-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="15479-151">**Rozsah:** Společnost</span><span class="sxs-lookup"><span data-stu-id="15479-151">**Scope:** Company</span></span> 
- <span data-ttu-id="15479-152">**Společnost:** CEU</span><span class="sxs-lookup"><span data-stu-id="15479-152">**Company:** CEU</span></span>

| <span data-ttu-id="15479-153">Segmenty</span><span class="sxs-lookup"><span data-stu-id="15479-153">Segments</span></span>  | <span data-ttu-id="15479-154">Typ segmentu</span><span class="sxs-lookup"><span data-stu-id="15479-154">Segment type</span></span> | <span data-ttu-id="15479-155">Hodnota</span><span class="sxs-lookup"><span data-stu-id="15479-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="15479-156">Segment 1</span><span class="sxs-lookup"><span data-stu-id="15479-156">Segment 1</span></span> | <span data-ttu-id="15479-157">Konstanta</span><span class="sxs-lookup"><span data-stu-id="15479-157">Constant</span></span>     | <span data-ttu-id="15479-158">PO-</span><span class="sxs-lookup"><span data-stu-id="15479-158">SO-</span></span>      |
| <span data-ttu-id="15479-159">Segment 2</span><span class="sxs-lookup"><span data-stu-id="15479-159">Segment 2</span></span> | <span data-ttu-id="15479-160">Alfanumerické</span><span class="sxs-lookup"><span data-stu-id="15479-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="15479-161">**Příklad formátovaného čísla**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="15479-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="15479-162">Přestože rozsah segmentu není zahrnut ve formátu, číslování bude restartováno pro každé ID společnosti.</span><span class="sxs-lookup"><span data-stu-id="15479-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="15479-163">Používáte-li pro všechna ID společností stejný formát, stejná čísla se používají v každé společnosti.</span><span class="sxs-lookup"><span data-stu-id="15479-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="15479-164">Například číslo prodejní objednávky SO-0029 je používáno v každé společnosti.</span><span class="sxs-lookup"><span data-stu-id="15479-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="15479-165">Můžete také změnit celý formát číselné řady pro ostatní ID společností.</span><span class="sxs-lookup"><span data-stu-id="15479-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="15479-166">Čísla nákupních žádanek</span><span class="sxs-lookup"><span data-stu-id="15479-166">Purchase requisition numbers</span></span>

<span data-ttu-id="15479-167">V následujícím příkladu jsou čísla nákupních žádanek používána pro celou organizaci.</span><span class="sxs-lookup"><span data-stu-id="15479-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="15479-168">**Oblast:** Nákup</span><span class="sxs-lookup"><span data-stu-id="15479-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="15479-169">**Odkaz:** Nákupní žádanka</span><span class="sxs-lookup"><span data-stu-id="15479-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="15479-170">**Rozsah:** Sdílené</span><span class="sxs-lookup"><span data-stu-id="15479-170">**Scope:** Shared</span></span>

| <span data-ttu-id="15479-171">Segmenty</span><span class="sxs-lookup"><span data-stu-id="15479-171">Segments</span></span>  | <span data-ttu-id="15479-172">Typ segmentu</span><span class="sxs-lookup"><span data-stu-id="15479-172">Segment type</span></span> | <span data-ttu-id="15479-173">Hodnota</span><span class="sxs-lookup"><span data-stu-id="15479-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="15479-174">Segment 1</span><span class="sxs-lookup"><span data-stu-id="15479-174">Segment 1</span></span> | <span data-ttu-id="15479-175">Konstanta</span><span class="sxs-lookup"><span data-stu-id="15479-175">Constant</span></span>     | <span data-ttu-id="15479-176">Žád</span><span class="sxs-lookup"><span data-stu-id="15479-176">Req</span></span>      |
| <span data-ttu-id="15479-177">Segment 2</span><span class="sxs-lookup"><span data-stu-id="15479-177">Segment 2</span></span> | <span data-ttu-id="15479-178">Alfanumerické</span><span class="sxs-lookup"><span data-stu-id="15479-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="15479-179">**Příklad formátovaného čísla**: Žád0052</span><span class="sxs-lookup"><span data-stu-id="15479-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="15479-180">Vzhledem k tomu, že rozsah je **Sdílené**, formát číselné řady se používá v rámci celé organizace.</span><span class="sxs-lookup"><span data-stu-id="15479-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="15479-181">Nemůžete nastavit různé formáty číselné řady pro různé části organizace.</span><span class="sxs-lookup"><span data-stu-id="15479-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="15479-182">Předpoklady ohledně výkonu pro číselné řady</span><span class="sxs-lookup"><span data-stu-id="15479-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="15479-183">Zvažte následující informace o způsobu konfigurace číselné řady mohou ovlivnit výkonnost systému před nastavením číselných řad.</span><span class="sxs-lookup"><span data-stu-id="15479-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="15479-184">Souvislé a nesouvislé číselné řady</span><span class="sxs-lookup"><span data-stu-id="15479-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="15479-185">Číselné řady mohou být souvislé nebo nesouvislé.</span><span class="sxs-lookup"><span data-stu-id="15479-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="15479-186">Souvislá číselná řadu nepřeskočí žádná čísla, ale čísla se nesmí používat postupně.</span><span class="sxs-lookup"><span data-stu-id="15479-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="15479-187">Čísla z nesouvislé číselné řady jsou používána postupně, ale sekvence může vynechat čísla.</span><span class="sxs-lookup"><span data-stu-id="15479-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="15479-188">Například pokud uživatel zruší transakcí, číslo se vygeneruje, ale nepoužije.</span><span class="sxs-lookup"><span data-stu-id="15479-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="15479-189">V souvislé číselné řadě se toto číslo použije později.</span><span class="sxs-lookup"><span data-stu-id="15479-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="15479-190">V nesouvislé číselné řadě toto číslo není použito.</span><span class="sxs-lookup"><span data-stu-id="15479-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="15479-191">Souvislé číselné řady jsou obvykle nutné pro externí dokumenty, jako jsou například nákupní objednávky, prodejní objednávky a faktury.</span><span class="sxs-lookup"><span data-stu-id="15479-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="15479-192">Avšak souvislé číselné řady mohou negativně ovlivnit čas odezvy systému vzhledem k tomu, že systém musí požadovat číslo z databáze při každém vytvoření nového dokumentu nebo záznamu.</span><span class="sxs-lookup"><span data-stu-id="15479-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="15479-193">Používáte-li nesouvislou číselnou řadu, můžete povolit možnost **Předběžné přidělení** na pevné záložce **Výkon** na stránce **Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="15479-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="15479-194">Při zadání množství čísel pro předběžné přidělení vybere systém tato čísla a uloží je do paměti.</span><span class="sxs-lookup"><span data-stu-id="15479-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="15479-195">Nová čísla jsou požadována z databáze, až poté, co bylo použito předběžně přidělené množství.</span><span class="sxs-lookup"><span data-stu-id="15479-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="15479-196">Pokud regulační předpis nepožaduje používání souvislé řady čísel, doporučujeme použít nesouvislé číselné řady pro lepší výkon.</span><span class="sxs-lookup"><span data-stu-id="15479-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="15479-197">Automatické vyčištění číselných řad</span><span class="sxs-lookup"><span data-stu-id="15479-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="15479-198">V případě výpadku napájení, chyby aplikace nebo jiného neočekávaného selhání nemůže systém znovu použít čísla pro souvislé číselné řady.</span><span class="sxs-lookup"><span data-stu-id="15479-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="15479-199">Proces čištění můžete spustit ručně nebo automaticky pro obnovení ztracených čísel.</span><span class="sxs-lookup"><span data-stu-id="15479-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="15479-200">Při plánování procesu čištění pečlivě zvažte použití serveru.</span><span class="sxs-lookup"><span data-stu-id="15479-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="15479-201">Čištění se doporučuje provádět jako dávková úloha mimo pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="15479-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






