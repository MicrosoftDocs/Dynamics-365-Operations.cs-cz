---
title: "Vykazování DPH pro Evropu"
description: "Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c0be253e80636d659027f69cbac58062cb28269e
ms.contentlocale: cs-cz
ms.lasthandoff: 07/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="d5556-103">Vykazování DPH pro Evropu</span><span class="sxs-lookup"><span data-stu-id="d5556-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d5556-104">Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.</span><span class="sxs-lookup"><span data-stu-id="d5556-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="d5556-105">Toto téma obsahuje obecný přístup k nastavení a generování výkazu DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="d5556-106">Tento přístup je společný pro uživatele v právnických osobách v těchto zemích a oblastech:</span><span class="sxs-lookup"><span data-stu-id="d5556-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="d5556-107">Rakousko</span><span class="sxs-lookup"><span data-stu-id="d5556-107">Austria</span></span>
-   <span data-ttu-id="d5556-108">Belgie</span><span class="sxs-lookup"><span data-stu-id="d5556-108">Belgium</span></span>
-   <span data-ttu-id="d5556-109">Česká republika</span><span class="sxs-lookup"><span data-stu-id="d5556-109">Czech Republic</span></span>
-   <span data-ttu-id="d5556-110">Estonsko</span><span class="sxs-lookup"><span data-stu-id="d5556-110">Estonia</span></span>
-   <span data-ttu-id="d5556-111">Finsko</span><span class="sxs-lookup"><span data-stu-id="d5556-111">Finland</span></span>
-   <span data-ttu-id="d5556-112">Německo</span><span class="sxs-lookup"><span data-stu-id="d5556-112">Germany</span></span>
-   <span data-ttu-id="d5556-113">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="d5556-113">Latvia</span></span>
-   <span data-ttu-id="d5556-114">Litva</span><span class="sxs-lookup"><span data-stu-id="d5556-114">Lithuania</span></span>
-   <span data-ttu-id="d5556-115">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="d5556-115">Netherlands</span></span>
-   <span data-ttu-id="d5556-116">Švédsko</span><span class="sxs-lookup"><span data-stu-id="d5556-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="d5556-117">Přehled výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="d5556-117">VAT statement overview</span></span>
<span data-ttu-id="d5556-118">Výkaz DPH je založený na částkách daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="d5556-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="d5556-119">Proces generování výkazu DPH je součástí procesu platby DPH, který je implementován pomocí funkce vypořádání a zaúčtování DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="d5556-120">Tato funkce se používá k výpočtu DPH splatné pro dané období.</span><span class="sxs-lookup"><span data-stu-id="d5556-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="d5556-121">Výpočet vyrovnání zahrnuje zaúčtovanou DPH pro vybrané období vyrovnání daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="d5556-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="d5556-122">Postup pro výpočet dat pro výkaz DPH je založen na vztahu mezi kódy DPH a kódy vykazování DPH, kde kódy vykazování daně odpovídají polím s výkazy DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="d5556-123">Pro každý kód DPH by měly být nastaveny kódy vykazování DPH pro každý typ transakce, například zdanitelné prodeje zdanitelné nákupy, zdanitelný import.</span><span class="sxs-lookup"><span data-stu-id="d5556-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="d5556-124">Tento typ transakcí je popsán v části Kódy DPH pro vykazování DPH dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="d5556-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="d5556-125">Pro každý kód vykazování by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5556-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="d5556-126">Ve stejnou dobu jsou kódy DPH propojeny s konkrétním finančním úřadem prostřednictvím období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="d5556-127">Pro každý finanční úřad pro vykazování DPH by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5556-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="d5556-128">Tedy pouze kódy vykazování DPH se stejným rozložením sestavy, která je nastavena pro finanční úřad k odvedení DPH v období vyrovnání DPH pro kód DPH lze vybrat v nastavení sestavy kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="d5556-129">Transakce DPH generované při účtování objednávky nebo deníku obsahují kód DPH, zdroj DPH, směr DPH a částky transakcí (částka základu daně a výše daně v zúčtovací měně, měně DPH a měně transakce).</span><span class="sxs-lookup"><span data-stu-id="d5556-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="d5556-130">V závislosti na kombinaci atributů transakce DPH, částky transakce tvoří celkové částky určené pro kódy vykazování DPH určené pro kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="d5556-131">Následující obrázek znázorňuje vztah mezi daty.</span><span class="sxs-lookup"><span data-stu-id="d5556-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="d5556-133">Nastavení výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="d5556-133">VAT statement setup</span></span>
<span data-ttu-id="d5556-134">Chcete-li generovat výkazy DPH, je nutné vytvořit následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="d5556-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="d5556-135">Nastavení daňových úřadů pro vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="d5556-135">Sales tax authorities for VAT reporting</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-authorities). -->
<span data-ttu-id="d5556-136">Dříve než můžete vytvořit kódy vykazování DPH, je nutné vybrat správnou sestavu rozložení pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="d5556-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="d5556-137">Na stránce **Finanční úřady** v části **Obecné** vyberte **Rozložení sestavy**.</span><span class="sxs-lookup"><span data-stu-id="d5556-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="d5556-138">Toto rozložení bude použito, když nastavujete kódy vykazování DPH.</span><span class="sxs-lookup"><span data-stu-id="d5556-138">This layout will be used when you set up sales tax reporting codes.</span></span>

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="d5556-139">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="d5556-139">Sales tax reporting codes</span></span>

<span data-ttu-id="d5556-140">Kódy vykazování DPH jsou pole kódy DPH výkazu nebo značky názvy ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="d5556-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="d5556-141">Tyto kódy se používají k agregaci a přípravě částky v sestavě.</span><span class="sxs-lookup"><span data-stu-id="d5556-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="d5556-142">Při konfiguraci elektronického formátu vykazování ve výkazu DPH budou použity názvy částek výsledku.</span><span class="sxs-lookup"><span data-stu-id="d5556-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="d5556-143">Můžete vytvářet a udržovat kódy vykazování DPH na stránce **Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="d5556-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="d5556-144">Každý kód je nutné přiřadit rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5556-144">You must assign each code a report layout.</span></span> <span data-ttu-id="d5556-145">Jakmile vytvoříte kódy vykazování DPH, můžete použít kódy v části **Nastavení sestavy** na stránce **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="d5556-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-reporting-codes).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="d5556-146">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="d5556-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](/dynamics365/unified-operations/financials/general-ledger/tasks/set-up-sales-tax-codes).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5556-147"><strong>Typ transakce</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="d5556-148"><strong>Popis transakcí a částek pro výpočet v typu transakce</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-149"><strong>Zdanitelné prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="d5556-150">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-151">Datum transakce je ve vybraném období/</span><span class="sxs-lookup"><span data-stu-id="d5556-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="d5556-152">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-153">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-154"><strong>Prodej bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="d5556-155">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-156">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-157">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="d5556-158">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-159"><strong>DPH na výstupu</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="d5556-160">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-161">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-162">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-163">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-164"><strong>Zdanitelný prodejní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-165">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-166">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-167">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-168">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-169"><strong>Prodejní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-170">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-171">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-172">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="d5556-173">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-174"><strong>DPH na prodejním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-175">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-176">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-177">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-178">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-179"><strong>Zdanitelné nákupy</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="d5556-180">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-181">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-182">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-183">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-184"><strong>Nákup bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="d5556-185">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-186">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-187">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="d5556-188">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-189"><strong>DPH na vstupu</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="d5556-190">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-191">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-192">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-193">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-194"><strong>Zdanitelný nákupní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-195">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-196">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-197">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-198">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-199"><strong>Nákupní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-200">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-201">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-202">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="d5556-203">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-204"><strong>DPH na nákupním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-205">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-206">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-207">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="d5556-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="d5556-208">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-209"><strong>Zdanitelný import</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="d5556-210">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-211">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-212"><strong>Směr daně</strong> je <strong>Použít daň</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="d5556-213">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-214"><strong>Protiúčet zdanitelného dovozu</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="d5556-215">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-216">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-217"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5556-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d5556-218">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-219"><strong>Zdanitelný dovozní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-220">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-221">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="d5556-222">e</span><span class="sxs-lookup"><span data-stu-id="d5556-222">e</span></span><li><span data-ttu-id="d5556-223"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5556-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d5556-224">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-225"><strong>Protiúčet zdanitelných dovozních dobropisů</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="d5556-226">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-227">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-228">Směr daně je <strong>Importní DPH</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5556-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="d5556-229">d</span><span class="sxs-lookup"><span data-stu-id="d5556-229">d</span></span><li><span data-ttu-id="d5556-230">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5556-231"><strong>Importní DPH</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="d5556-232">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-233">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-234"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5556-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d5556-235">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5556-236"><strong>Zapsat importní DPH na protiúčet</strong></span><span class="sxs-lookup"><span data-stu-id="d5556-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="d5556-237">Stornovaný součet <strong>Částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d5556-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="d5556-238">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="d5556-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="d5556-239"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5556-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="d5556-240">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="d5556-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d5556-241">Pro výše uvedenou tabulku se předpokládá, že jsou splněna tato kritéria:</span><span class="sxs-lookup"><span data-stu-id="d5556-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="d5556-242">Částka základu daně je částka transakce z pole **Původ v zúčtovací měně**.</span><span class="sxs-lookup"><span data-stu-id="d5556-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="d5556-243">Částka základu daně je částka transakce z pole **Částka daně skutečných prodejů**.</span><span class="sxs-lookup"><span data-stu-id="d5556-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="d5556-244">Konfigurace modelu ER a formátu výkazu</span><span class="sxs-lookup"><span data-stu-id="d5556-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="d5556-245">Elektronické hlášení (ER) můžete použít ke konfiguraci výkazů a sestav a k exportu různých formátů elektronických dat bez nutnosti změny kódu X ++.</span><span class="sxs-lookup"><span data-stu-id="d5556-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="d5556-246">Další informace:</span><span class="sxs-lookup"><span data-stu-id="d5556-246">For additional information:</span></span>

-   [<span data-ttu-id="d5556-247">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d5556-247">Electronic reporting overview</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)
-   [<span data-ttu-id="d5556-248">Stažení konfigurace elektronického vykazování ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="d5556-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
-   [<span data-ttu-id="d5556-249">Požadavky na lokalizaci – vytvoření konfigurace GER</span><span class="sxs-lookup"><span data-stu-id="d5556-249">Localization requirements – Create a GER configuration</span></span>](/dynamics365/unified-operations/dev-itpro/analytics/electronic-reporting-configuration)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="d5556-250">Prostředky pro výkazy DPH specifické podle zemí</span><span class="sxs-lookup"><span data-stu-id="d5556-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="d5556-251">Výkaz DPH pro každou zemi musí splňovat požadavky právních předpisů této země.</span><span class="sxs-lookup"><span data-stu-id="d5556-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="d5556-252">Existují předdefinované obecné modely a formáty výkazů DPH pro země uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="d5556-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="d5556-253">Země</span><span class="sxs-lookup"><span data-stu-id="d5556-253">Country</span></span>        | <span data-ttu-id="d5556-254">Doplňkové informace</span><span class="sxs-lookup"><span data-stu-id="d5556-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d5556-255">Rakousko</span><span class="sxs-lookup"><span data-stu-id="d5556-255">Austria</span></span>        |  [<span data-ttu-id="d5556-256">Podrobnosti výkazu DPH pro Rakousko</span><span class="sxs-lookup"><span data-stu-id="d5556-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="d5556-257">Belgie</span><span class="sxs-lookup"><span data-stu-id="d5556-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="d5556-258">Česká republika</span><span class="sxs-lookup"><span data-stu-id="d5556-258">Czech Republic</span></span> |  [<span data-ttu-id="d5556-259">Podrobnosti výkazu DPH pro Českou republiku</span><span class="sxs-lookup"><span data-stu-id="d5556-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="d5556-260">Estonsko</span><span class="sxs-lookup"><span data-stu-id="d5556-260">Estonia</span></span>        |  [<span data-ttu-id="d5556-261">Podrobnosti výkazu DPH pro Estonsko</span><span class="sxs-lookup"><span data-stu-id="d5556-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="d5556-262">Finsko</span><span class="sxs-lookup"><span data-stu-id="d5556-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="d5556-263">Německo</span><span class="sxs-lookup"><span data-stu-id="d5556-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="d5556-264">Itálie</span><span class="sxs-lookup"><span data-stu-id="d5556-264">Italy</span></span>          | [<span data-ttu-id="d5556-265">Podrobnosti výkazu DPH pro Itálii</span><span class="sxs-lookup"><span data-stu-id="d5556-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="d5556-266">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="d5556-266">Latvia</span></span>         | [<span data-ttu-id="d5556-267">Podrobnosti výkazu DPH pro Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="d5556-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="d5556-268">Litva</span><span class="sxs-lookup"><span data-stu-id="d5556-268">Lithuania</span></span>      | [<span data-ttu-id="d5556-269">Podrobnosti výkazu DPH pro Litvu</span><span class="sxs-lookup"><span data-stu-id="d5556-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="d5556-270">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="d5556-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="d5556-271">Švédsko</span><span class="sxs-lookup"><span data-stu-id="d5556-271">Sweden</span></span>         |                                                                                 |






