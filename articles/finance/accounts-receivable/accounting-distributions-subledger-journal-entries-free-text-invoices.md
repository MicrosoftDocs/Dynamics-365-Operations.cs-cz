---
title: Rozúčtování a položky deníku pro volné faktury
description: Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách. Každá částka, která musí být zaúčtována, když je volná faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d5b35347d63bffbf5b9261cbd93f49120ded19a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248056"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a><span data-ttu-id="2b874-104">Rozúčtování a položky dílčí hlavní knihy pro volné faktury</span><span class="sxs-lookup"><span data-stu-id="2b874-104">Accounting distributions and subledger entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b874-105">Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách.</span><span class="sxs-lookup"><span data-stu-id="2b874-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="2b874-106">Každá částka, která musí být zaúčtována, když je volná faktura zapsána do deníku, bude mít jedno nebo více rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="2b874-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="2b874-107">Rozúčtování</span><span class="sxs-lookup"><span data-stu-id="2b874-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="2b874-108">Na stránce Volné faktury můžete použít následující tlačítka k zobrazení a případné změně rozúčtování pro každou částku na volné faktuře.</span><span class="sxs-lookup"><span data-stu-id="2b874-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="2b874-109">**Distribuovat částky**—Zobrazení a změna rozúčtování pro každý řádek a také všechny podřízené řádky, jako jsou například daně a poplatky.</span><span class="sxs-lookup"><span data-stu-id="2b874-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="2b874-110">Lze také zobrazit a změnit rozúčtování pro podřízený řádek přímo na stránce Transakcí DPH nebo na stránce Transakce nákladů.</span><span class="sxs-lookup"><span data-stu-id="2b874-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="2b874-111">Změna částek v záhlaví volných faktur, například náklady nebo měnové zaokrouhlení částky.</span><span class="sxs-lookup"><span data-stu-id="2b874-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="2b874-112">Změna částek na řádcích volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="2b874-113">**Zobrazit distribuce** – Zobrazení rozúčtování pro všechny řádky v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="2b874-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="2b874-114">V tomto zobrazení nelze měnit rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="2b874-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="2b874-115">Zobrazení záhlaví a částek řádku.</span><span class="sxs-lookup"><span data-stu-id="2b874-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="2b874-116">Distribuce částek</span><span class="sxs-lookup"><span data-stu-id="2b874-116">Distributing amounts</span></span>
<span data-ttu-id="2b874-117">Při vkládání volné faktury budou jednotlivé částky rozděleny následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2b874-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b874-118">Typ peněžní částky</span><span class="sxs-lookup"><span data-stu-id="2b874-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="2b874-119">Odkud se zobrazuje hlavní účet</span><span class="sxs-lookup"><span data-stu-id="2b874-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="2b874-120">Pořadí priority, které určuje, jaká výchozí finanční dimenze je zobrazena</span><span class="sxs-lookup"><span data-stu-id="2b874-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b874-121">Řádek volné faktury</span><span class="sxs-lookup"><span data-stu-id="2b874-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="2b874-122">Hlavní kniha na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="2b874-123">Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</span><span class="sxs-lookup"><span data-stu-id="2b874-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="2b874-124">Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-125">Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-126">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="2b874-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b874-127">Řádek volné faktury pro kombinaci čísla dlouhodobého majetku a oceňovacího modelu</span><span class="sxs-lookup"><span data-stu-id="2b874-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2b874-128"><strong>Poznámka </strong></span><span class="sxs-lookup"><span data-stu-id="2b874-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b874-129">Hlavní účet na řádku volné faktury bude účet vyřazení dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="2b874-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="2b874-130">Hlavní kniha na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="2b874-131">Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-132">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="2b874-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b874-133">Částka slevy na volné faktuře</span><span class="sxs-lookup"><span data-stu-id="2b874-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="2b874-134">Pole Hlavní účet pro slevy odběratele na stránce strany Platební slevy.</span><span class="sxs-lookup"><span data-stu-id="2b874-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="2b874-135">Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</span><span class="sxs-lookup"><span data-stu-id="2b874-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="2b874-136">Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-137">Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-138">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="2b874-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b874-139">Částka DPH na volné faktuře</span><span class="sxs-lookup"><span data-stu-id="2b874-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="2b874-140">Pole Splatná DPH na stránce Skupiny zaúčtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="2b874-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="2b874-141">Použijte finanční dimenze, které jsou definovány v částce řádku na volné faktuře nebo distribucí pro částky řádku nákladů.</span><span class="sxs-lookup"><span data-stu-id="2b874-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="2b874-142">Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-143">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="2b874-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2b874-144">Částka na řádku nákladů na volné faktuře</span><span class="sxs-lookup"><span data-stu-id="2b874-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="2b874-145">Pole Účet Dal na stránce Kódy nákladů.</span><span class="sxs-lookup"><span data-stu-id="2b874-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="2b874-146">Je-li hlavní účet účet přidělení, použijte výchozí hodnotu z definice účtu přidělení.</span><span class="sxs-lookup"><span data-stu-id="2b874-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="2b874-147">Pokud hlavní účet není účtem přidělení, použijte výchozí šablonu finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-148">Použijte výchozí hodnoty finanční dimenze na řádku volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="2b874-149">Použijte výchozí hodnoty finanční dimenze z hlavního účtu na stránce Účtová osnova.</span><span class="sxs-lookup"><span data-stu-id="2b874-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="2b874-150">Distribuce daní</span><span class="sxs-lookup"><span data-stu-id="2b874-150">Distributing taxes</span></span>
<span data-ttu-id="2b874-151">Dokud daně nejsou vypočítány, nelze pro ně vytvořit rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="2b874-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="2b874-152">Při výpočtu DPH je třeba ve formuláři Volná faktura provést jeden z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="2b874-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="2b874-153">Zobrazit DPH.</span><span class="sxs-lookup"><span data-stu-id="2b874-153">View the sales tax.</span></span>
-   <span data-ttu-id="2b874-154">Zobrazit celkový součet faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-154">View the invoice total.</span></span>
-   <span data-ttu-id="2b874-155">Zobrazit cashflow.</span><span class="sxs-lookup"><span data-stu-id="2b874-155">View the cash flow.</span></span>
-   <span data-ttu-id="2b874-156">Zobrazit rozúčtování pro všechny volné faktury.</span><span class="sxs-lookup"><span data-stu-id="2b874-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="2b874-157">Zobrazit dílčí hlavní knihu.</span><span class="sxs-lookup"><span data-stu-id="2b874-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="2b874-158"> Dílčí hlavní knihy pro volné faktury</span><span class="sxs-lookup"><span data-stu-id="2b874-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="2b874-159">Před zaúčtováním volné faktury můžete zobrazit celý účetní zápis faktury, který zahrnuje pohledávky a závazky, abyste ověřili, zda je faktura zaúčtována na správné účty.</span><span class="sxs-lookup"><span data-stu-id="2b874-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="2b874-160">Toto zobrazení celkového zápisu do účetnictví se nazývá dílčí hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="2b874-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="2b874-161">Pokud zobrazíte náhled dříve, než zapíšete fakturu dodavatele do deníku, a položka dílčí hlavní knihy není správná, nelze položku dílčí hlavní knihy změnit.</span><span class="sxs-lookup"><span data-stu-id="2b874-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="2b874-162">Namísto toho je nutné změnit rozúčtování nebo účetní profil.</span><span class="sxs-lookup"><span data-stu-id="2b874-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="2b874-163">Rozúčtování slouží k definování jedné strany účetní položky, má dáti nebo dal.</span><span class="sxs-lookup"><span data-stu-id="2b874-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="2b874-164">Vyrovnání účetní položky dílčí hlavní knihy je vytvořeno z účetních profilů, jako je například účet odběratele nebo daň.</span><span class="sxs-lookup"><span data-stu-id="2b874-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]