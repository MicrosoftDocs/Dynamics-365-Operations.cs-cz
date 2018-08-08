---
title: Pravidla eliminace
description: "V tomto tématu jsou informace o pravidlech eliminace a různých možnostech pro vytváření sestav o eliminacích."
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: c0736d63c9a582948d197dc267f9941cbbd3e3c6
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="elimination-rules"></a><span data-ttu-id="feee9-103">Pravidla eliminace</span><span class="sxs-lookup"><span data-stu-id="feee9-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feee9-104">V tomto tématu jsou informace o pravidlech eliminace a různých možnostech pro vytváření sestav o eliminacích.</span><span class="sxs-lookup"><span data-stu-id="feee9-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="feee9-105">Transakce eliminací se používají v případech, kdy nadřazená právnická osoba obchoduje s některými dceřinými právnickými osobami a přitom je používáno konsolidované finanční vykazování.</span><span class="sxs-lookup"><span data-stu-id="feee9-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="feee9-106">Konsolidované finanční výkazy musí zahrnovat pouze transakce, které probíhají mezi konsolidovanou organizací a dalšími entitami mimo dané organizace.</span><span class="sxs-lookup"><span data-stu-id="feee9-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="feee9-107">Transakce mezi právnickými osobami, které jsou součástí stejné organizace, je proto třeba odebrat nebo odstranit z hlavní knihy tak, aby se nezobrazily ve finančních výkazech.</span><span class="sxs-lookup"><span data-stu-id="feee9-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="feee9-108">Existuje několik způsobů, jak vykázat eliminace:</span><span class="sxs-lookup"><span data-stu-id="feee9-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="feee9-109">Pravidlo eliminace lze vytvořit a zpracovat v konsolidaci nebo eliminaci společnosti.</span><span class="sxs-lookup"><span data-stu-id="feee9-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="feee9-110">Finanční sestavy slouží k zobrazení účtů a dimenzí eliminací u konkrétního řádku nebo sloupce.</span><span class="sxs-lookup"><span data-stu-id="feee9-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="feee9-111">Samostatnou právnickou osobu lze použít k zaúčtování položek transakce ke sledování eliminací.</span><span class="sxs-lookup"><span data-stu-id="feee9-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="feee9-112">Toto téma se zaměřuje na pravidla eliminace, která jsou zpracována ve společnosti konsolidace nebo eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="feee9-113">Můžete konfigurovat pravidla eliminace pro vytvoření transakcí eliminace u právnické osoby, která je určena jako cílová právnická osoba pro eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="feee9-114">Tato cílová právnická osoba se také nazývá právnická osoba eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="feee9-115">Deníky eliminace lze vygenerovat během procesu konsolidací nebo pomocí návrhu deníku eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="feee9-116">Před nastavením pravidel eliminace se doporučuje důkladné obeznámení s následujícími termíny:</span><span class="sxs-lookup"><span data-stu-id="feee9-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="feee9-117">**Zdrojová právnická osoba** – právnická osoba, pro kterou byly zaúčtovány částky, které jsou právě eliminovány.</span><span class="sxs-lookup"><span data-stu-id="feee9-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="feee9-118">**Cílová právnická osoba** - právnická osoba, pro kterou jsou zaúčtována pravidla eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="feee9-119">**Právnická osoba eliminace** - právnická osoba určená jako cílová právnická osoba pro eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="feee9-120">**Konsolidační právnická osoba** - právnická osoba vytvořená s cílem vykazování finančních výsledků pro určitou skupinu právnických osob.</span><span class="sxs-lookup"><span data-stu-id="feee9-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="feee9-121">K této právnické osoby jsou konsolidována finanční data z daných právnických osob a poté je na základě kombinovaných dat vytvořena finanční sestava.</span><span class="sxs-lookup"><span data-stu-id="feee9-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="feee9-122">V následující tabulce jsou uvedeny typy transakcí, které mohou mít eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="feee9-123">Typ transakce</span><span class="sxs-lookup"><span data-stu-id="feee9-123">Transaction type</span></span></th>
<th><span data-ttu-id="feee9-124">Příklad</span><span class="sxs-lookup"><span data-stu-id="feee9-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="feee9-125">Zadání a fakturace prodejní objednávky (centralizované zpracování)</span><span class="sxs-lookup"><span data-stu-id="feee9-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="feee9-126">Prodej produktu odběrateli v zastoupení jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-127">Zadání prodejní objednávky (mezi společnostmi/v rámci jedné společnosti) a fakturace</span><span class="sxs-lookup"><span data-stu-id="feee9-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="feee9-128">Prodej produktů mezi právnickými osobami ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="feee9-129">Nákupní objednávky (centralizované zpracování)</span><span class="sxs-lookup"><span data-stu-id="feee9-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="feee9-130">Nákup skladových zásob, materiálu, služeb, dlouhodobého majetku a dalších produktů od dodavatele v zastoupení jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-131">Řízení zásob (mezi různými společnostmi/v rámci jedné společnosti)</span><span class="sxs-lookup"><span data-stu-id="feee9-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="feee9-132">Převod zásob jedné právnické osoby na dlouhodobý majetek jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="feee9-133">Převod zásob jedné právnické osoby na zásoby jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="feee9-134">Sledování zásob během tranzitu</span><span class="sxs-lookup"><span data-stu-id="feee9-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="feee9-135">Převod položek mezi sklady stejné právnické osoby, která se ale nachází na různých místech.</span><span class="sxs-lookup"><span data-stu-id="feee9-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-136">Centralizované zpracování faktur s ohledem na závazky</span><span class="sxs-lookup"><span data-stu-id="feee9-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="feee9-137">Zaznamenání faktury v zastoupení jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="feee9-138">Centralizované zpracování plateb s ohledem na závazky</span><span class="sxs-lookup"><span data-stu-id="feee9-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="feee9-139">Zaplacení faktury v zastoupení jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-140">Řízení hotovosti a pokladna (centralizované zpracování)</span><span class="sxs-lookup"><span data-stu-id="feee9-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="feee9-141">Zpracování plateb daní, refundací daní, účtování úroků, půjček, záloh, vyplácení dividend a předem placených honorářů nebo provizí.</span><span class="sxs-lookup"><span data-stu-id="feee9-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="feee9-142">Zaplacení výdajů v zastoupení jiné právnické osoby ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="feee9-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="feee9-143">Faktura je zadána do knihy cílové právnické osoby a je nutné zajistit kombinované vyrovnání mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="feee9-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="feee9-144">Například jedna právnická osoba zaplatí výdaje vyúčtované zaměstnanci u jiné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="feee9-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="feee9-145">V tomto případě vyúčtování výdajů zaměstnanci bude obsahovat výdaje, které se vztahují k jiné právnické osobě.</span><span class="sxs-lookup"><span data-stu-id="feee9-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="feee9-146">Převod hotovosti od jedné právnické osoby jiné v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="feee9-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="feee9-147">Pohledávky (centralizované zpracování)</span><span class="sxs-lookup"><span data-stu-id="feee9-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="feee9-148">Příjem hotovosti za odběratelskou fakturu jiné právnické osoby a uložení šeku na bankovní účet této právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="feee9-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-149">Mzdy (centralizované zpracování, mezipodnikové/vnitropodnikové)</span><span class="sxs-lookup"><span data-stu-id="feee9-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="feee9-150">Platba mezd jiné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="feee9-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="feee9-151">Právnická osoba může například vyplácet vlastní mzdy svým zaměstnancům, avšak nechá si v rámci zpracování mezd proplatit práci, kterou daný zaměstnanec vykonal pro jinou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="feee9-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="feee9-152">Případně určitý zaměstnanec pracoval na půl úvazku pro právnickou osobu A a na půl úvazku pro právnickou osobu B – výhody se vztahují na celou mzdu.</span><span class="sxs-lookup"><span data-stu-id="feee9-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="feee9-153">V takovém případě zahrnuje mzda zaměstnance platbu od obou právnických osob.</span><span class="sxs-lookup"><span data-stu-id="feee9-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="feee9-154">Nejsou zaúčtovány pouze vlastní platy, ale také daně, výhody (benefity), srážky a časové rozlišení platů.</span><span class="sxs-lookup"><span data-stu-id="feee9-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="feee9-155">Převody pracovních smluv z jednoho oddělení (divize) do jiného oddělení (divize).</span><span class="sxs-lookup"><span data-stu-id="feee9-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="feee9-156">Dlouhodobý majetek (mezipodnikový/vnitropodnikový)</span><span class="sxs-lookup"><span data-stu-id="feee9-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="feee9-157">Převod dlouhodobého majetku na dlouhodobý majetek nebo zásoby jiné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="feee9-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="feee9-158">Alokace (mezipodnikové/vnitropodnikové)</span><span class="sxs-lookup"><span data-stu-id="feee9-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="feee9-159">Zpracování podnikových přidělení.</span><span class="sxs-lookup"><span data-stu-id="feee9-159">You process corporate allocations.</span></span> <span data-ttu-id="feee9-160">Přidělení jsou aktivity prováděné pro libovolný přidělený účet, bez ohledu na zdrojový modul.</span><span class="sxs-lookup"><span data-stu-id="feee9-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="feee9-161">Příklad</span><span class="sxs-lookup"><span data-stu-id="feee9-161">Example</span></span>
<span data-ttu-id="feee9-162">Vaše právnická osoba, právnická osoba A prodává určité produkty jiné právnické osobě ve vaší organizaci, právnické osobě B. Následující příklad ukazuje, jak lze eliminovat transakce mezi dvěma právnickými osobami:</span><span class="sxs-lookup"><span data-stu-id="feee9-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="feee9-163">Právnická osoba A prodá produkt v ceně 10,00 jednotek právnické osobě B za cenu 10,00 jednotek.</span><span class="sxs-lookup"><span data-stu-id="feee9-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="feee9-164">Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za 10,00 jednotek plus 2,00 jednotky jako náklady na dopravu.</span><span class="sxs-lookup"><span data-stu-id="feee9-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="feee9-165">Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za cenu 15,00 jednotek a nárokuje si marži z prodeje.</span><span class="sxs-lookup"><span data-stu-id="feee9-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="feee9-166">Právnická osoba A prodává produkt v ceně 10,00 jednotek právnické osobě B za cenu 15,00 jednotek a nárokuje si polovinu marže z prodeje.</span><span class="sxs-lookup"><span data-stu-id="feee9-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="feee9-167">Právnická osoba B si nárokuje druhou polovinu marže z prodeje.</span><span class="sxs-lookup"><span data-stu-id="feee9-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="feee9-168">Proto je výnos rozdělen.</span><span class="sxs-lookup"><span data-stu-id="feee9-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="feee9-169">Rozdělení výnosů přináší motivaci pro objednávku od jiné právnické osoby v rámci organizace namísto objednávky od externí organizace.</span><span class="sxs-lookup"><span data-stu-id="feee9-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="feee9-170">Všechny tyto operace vedou k tomu, že vnitropodnikové transakce jsou zaúčtovávány na debetní a kreditní účty.</span><span class="sxs-lookup"><span data-stu-id="feee9-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="feee9-171">Kromě toho mohou tyto transakce zahrnovat částky přirážek nebo srážek, zejména pokud výše vnitropodnikových prodejů neodpovídá nákladům na prodané zboží.</span><span class="sxs-lookup"><span data-stu-id="feee9-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="feee9-172">Nastavení pravidel eliminace</span><span class="sxs-lookup"><span data-stu-id="feee9-172">Set up elimination rules</span></span>
<span data-ttu-id="feee9-173">Při nastavování pravidel eliminace v aplikaci Microsoft Dynamics 365 for Finance and Operations doporučujeme, abyste vytvořili finanční dimenzi konkrétně pro účely eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="feee9-174">Většina zákazníků jí nazývá obchodní partner nebo podobně.</span><span class="sxs-lookup"><span data-stu-id="feee9-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="feee9-175">Pokud se rozhodnete nepoužít finanční dimenzi, pak je nutné mít hlavní účty, které jsou specifické pro pouze mezipodnikové transakce.</span><span class="sxs-lookup"><span data-stu-id="feee9-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="feee9-176">Nastavení pro eliminace naleznete v části Nastavení modulu Konsolidace.</span><span class="sxs-lookup"><span data-stu-id="feee9-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="feee9-177">Jakmile zadáte popis pravidla, je třeba vybrat společnost, do které bude deník eliminace účtovat.</span><span class="sxs-lookup"><span data-stu-id="feee9-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="feee9-178">Mělo by se jednat o společnost, která má vybranou volbu **Použít pro proces finanční eliminace** v nastavení právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="feee9-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="feee9-179">Můžete nastavit datum, kdy se pravidlo eliminace stane platným, a v případě potřeby i datum jeho vypršení.</span><span class="sxs-lookup"><span data-stu-id="feee9-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="feee9-180">Musíte nastavit volbu **Aktivní** na **Ano**, pokud chcete, aby byla k dispozici v procesu návrhu eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="feee9-181">Vyberte název deníku, který má typ **Eliminace**.</span><span class="sxs-lookup"><span data-stu-id="feee9-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="feee9-182">Po definování základů můžete určit skutečná pravidla zpracování kliknutím na možnost **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="feee9-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="feee9-183">Existují dvě možnosti pro eliminace - eliminace změny čisté částky nebo určení pevné částky.</span><span class="sxs-lookup"><span data-stu-id="feee9-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="feee9-184">Vyberte svůj zdrojový účet.</span><span class="sxs-lookup"><span data-stu-id="feee9-184">Select your source account.</span></span> <span data-ttu-id="feee9-185">Jako zástupný znak můžete použít hvězdičku (\*).</span><span class="sxs-lookup"><span data-stu-id="feee9-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="feee9-186">Například hodnota 1\* by zvolila jako zdroj dat pro přidělení všechny účty začínající číslem 1.</span><span class="sxs-lookup"><span data-stu-id="feee9-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="feee9-187">Po výběru svých zdrojových účtů určí položka **Specifikace účtu** účet z cílové společnosti, která je použita.</span><span class="sxs-lookup"><span data-stu-id="feee9-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="feee9-188">Vyberte **Zdroj**, pokud chcete použít stejný hlavní účet definovaný v účtu **Zdroj**.</span><span class="sxs-lookup"><span data-stu-id="feee9-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="feee9-189">Vyberete-li možnost **Definováno uživatelem**, pak je nutné zadat cílový účet.</span><span class="sxs-lookup"><span data-stu-id="feee9-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="feee9-190">Specifikace dimenze funguje stejným způsobem.</span><span class="sxs-lookup"><span data-stu-id="feee9-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="feee9-191">Vyberete-li **Zdroj**, použijí se v cílové společnosti stejné dimenze jako ve zdrojové společnosti.</span><span class="sxs-lookup"><span data-stu-id="feee9-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="feee9-192">Vyberete-li **Definováno uživatelem**, je třeba určit dimenze v cílové společnosti kliknutím na položku nabídky **Cílové dimenze**.</span><span class="sxs-lookup"><span data-stu-id="feee9-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="feee9-193">Vyberte zdrojové dimenze, finanční dimenze a hodnoty, které slouží jako zdroj eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="feee9-194">Zpracování eliminační transakce</span><span class="sxs-lookup"><span data-stu-id="feee9-194">Process elimination transactions</span></span>
<span data-ttu-id="feee9-195">Existují dva způsoby zpracování transakcí eliminace - během konsolidovaného online procesu nebo vytvořením deníku eliminace a spuštěním procesu návrhu eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="feee9-196">Tato část se zaměřuje na vytváření deníku a spuštění procesu eliminace.</span><span class="sxs-lookup"><span data-stu-id="feee9-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="feee9-197">Ve společnosti určené jako společnost eliminace vyberte možnost **Deník eliminace** v modulu Konsolidace.</span><span class="sxs-lookup"><span data-stu-id="feee9-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="feee9-198">Po vybrání názvu deníku klikněte na položku **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="feee9-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="feee9-199">Návrh lze spustit výběrem nabídky **Návrhy** a potom výběrem možnosti **Návrh eliminace**.</span><span class="sxs-lookup"><span data-stu-id="feee9-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="feee9-200">Vyberte společnost, která je zdrojem konsolidovaných dat, a pak vyberte pravidlo, které chcete zpracovat.</span><span class="sxs-lookup"><span data-stu-id="feee9-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="feee9-201">Zadejte počáteční datum pro zahájení vyhledávání částek eliminace a koncové datum pro ukončení hledání data pro odstranění částky.</span><span class="sxs-lookup"><span data-stu-id="feee9-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="feee9-202">Pole **Datum zaúčtování do hlavní knihy** představuje datum použité pro zaúčtování deníku do hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="feee9-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="feee9-203">Po kliknutí na tlačítko **OK** můžete zkontrolovat částky a zaúčtovat deník.</span><span class="sxs-lookup"><span data-stu-id="feee9-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




