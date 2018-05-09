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
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c5cd61c45eb7cbc6f040f054a99d9a54e1ee854
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="e6b8f-103">Vykazování DPH pro Evropu</span><span class="sxs-lookup"><span data-stu-id="e6b8f-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6b8f-104">Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="e6b8f-105">Toto téma obsahuje obecný přístup k nastavení a generování výkazu DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="e6b8f-106">Tento přístup je společný pro uživatele v právnických osobách v těchto zemích a oblastech:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="e6b8f-107">Rakousko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-107">Austria</span></span>
-   <span data-ttu-id="e6b8f-108">Belgie</span><span class="sxs-lookup"><span data-stu-id="e6b8f-108">Belgium</span></span>
-   <span data-ttu-id="e6b8f-109">Česká republika</span><span class="sxs-lookup"><span data-stu-id="e6b8f-109">Czech Republic</span></span>
-   <span data-ttu-id="e6b8f-110">Estonsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-110">Estonia</span></span>
-   <span data-ttu-id="e6b8f-111">Finsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-111">Finland</span></span>
-   <span data-ttu-id="e6b8f-112">Německo</span><span class="sxs-lookup"><span data-stu-id="e6b8f-112">Germany</span></span>
-   <span data-ttu-id="e6b8f-113">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-113">Latvia</span></span>
-   <span data-ttu-id="e6b8f-114">Litva</span><span class="sxs-lookup"><span data-stu-id="e6b8f-114">Lithuania</span></span>
-   <span data-ttu-id="e6b8f-115">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-115">Netherlands</span></span>
-   <span data-ttu-id="e6b8f-116">Švédsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="e6b8f-117">Přehled výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="e6b8f-117">VAT statement overview</span></span>
<span data-ttu-id="e6b8f-118">Výkaz DPH je založený na částkách daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="e6b8f-119">Proces generování výkazu DPH je součástí procesu platby DPH, který je implementován pomocí funkce vypořádání a zaúčtování DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="e6b8f-120">Tato funkce se používá k výpočtu DPH splatné pro dané období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="e6b8f-121">Výpočet vyrovnání zahrnuje zaúčtovanou DPH pro vybrané období vyrovnání daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="e6b8f-122">Postup pro výpočet dat pro výkaz DPH je založen na vztahu mezi kódy DPH a kódy vykazování DPH, kde kódy vykazování daně odpovídají polím s výkazy DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="e6b8f-123">Pro každý kód DPH by měly být nastaveny kódy vykazování DPH pro každý typ transakce, například zdanitelné prodeje zdanitelné nákupy, zdanitelný import.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="e6b8f-124">Tento typ transakcí je popsán v části Kódy DPH pro vykazování DPH dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="e6b8f-125">Pro každý kód vykazování by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="e6b8f-126">Ve stejnou dobu jsou kódy DPH propojeny s konkrétním finančním úřadem prostřednictvím období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="e6b8f-127">Pro každý finanční úřad pro vykazování DPH by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="e6b8f-128">Tedy pouze kódy vykazování DPH se stejným rozložením sestavy, která je nastavena pro finanční úřad k odvedení DPH v období vyrovnání DPH pro kód DPH lze vybrat v nastavení sestavy kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="e6b8f-129">Transakce DPH generované při účtování objednávky nebo deníku obsahují kód DPH, zdroj DPH, směr DPH a částky transakcí (částka základu daně a výše daně v zúčtovací měně, měně DPH a měně transakce).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="e6b8f-130">V závislosti na kombinaci atributů transakce DPH, částky transakce tvoří celkové částky určené pro kódy vykazování DPH určené pro kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="e6b8f-131">Následující obrázek znázorňuje vztah mezi daty.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="e6b8f-133">Nastavení výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="e6b8f-133">VAT statement setup</span></span>
<span data-ttu-id="e6b8f-134">Chcete-li generovat výkazy DPH, je nutné vytvořit následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="e6b8f-135">Nastavení daňových úřadů pro vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="e6b8f-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="e6b8f-136">Dříve než můžete vytvořit kódy vykazování DPH, je nutné vybrat správnou sestavu rozložení pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="e6b8f-137">Na stránce **Finanční úřady** v části **Obecné** vyberte **Rozložení sestavy**.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="e6b8f-138">Toto rozložení bude použito, když nastavujete kódy vykazování DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="e6b8f-139">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="e6b8f-139">Sales tax reporting codes</span></span>

<span data-ttu-id="e6b8f-140">Kódy vykazování DPH jsou pole kódy DPH výkazu nebo značky názvy ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="e6b8f-141">Tyto kódy se používají k agregaci a přípravě částky v sestavě.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="e6b8f-142">Při konfiguraci elektronického formátu vykazování ve výkazu DPH budou použity názvy částek výsledku.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="e6b8f-143">Můžete vytvářet a udržovat kódy vykazování DPH na stránce **Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="e6b8f-144">Každý kód je nutné přiřadit rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-144">You must assign each code a report layout.</span></span> <span data-ttu-id="e6b8f-145">Jakmile vytvoříte kódy vykazování DPH, můžete použít kódy v části **Nastavení sestavy** na stránce **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="e6b8f-146">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="e6b8f-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="e6b8f-147">Stránka <!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Kódy DPH</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="e6b8f-148">Následující tabulka popisuje typy transakcí v nastavení sestavy pro kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="e6b8f-149">Výpočet zahrnuje transakce pro všechny typy zdrojů s výjimkou DPH.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6b8f-150"><strong>Typ transakce</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="e6b8f-151"><strong>Popis transakcí a částek pro výpočet v typu transakce</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-152"><strong>Zdanitelné prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="e6b8f-153">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-154">Datum transakce je ve vybraném období/</span><span class="sxs-lookup"><span data-stu-id="e6b8f-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="e6b8f-155">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-156">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-157"><strong>Prodej bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="e6b8f-158">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-159">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-160">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-161">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-162"><strong>DPH na výstupu</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="e6b8f-163">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-164">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-165">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-166">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-167"><strong>Zdanitelný prodejní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-168">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-169">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-170">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-171">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-172"><strong>Prodejní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-173">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-174">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-175">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-176">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-177"><strong>DPH na prodejním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-178">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-179">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-180">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-181">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-182"><strong>Zdanitelné nákupy</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="e6b8f-183">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-184">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-185">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-186">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-187"><strong>Nákup bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="e6b8f-188">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-189">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-190">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-191">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-192"><strong>DPH na vstupu</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="e6b8f-193">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-194">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-195">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-196">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-197"><strong>Zdanitelný nákupní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-198">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-199">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-200">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-201">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-202"><strong>Nákupní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-203">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-204">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-205">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-206">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-207"><strong>DPH na nákupním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-208">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-209">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-210">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="e6b8f-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="e6b8f-211">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-212"><strong>Zdanitelný import</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="e6b8f-213">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-214">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-215"><strong>Směr daně</strong> je <strong>Použít daň</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="e6b8f-216">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-217"><strong>Protiúčet zdanitelného dovozu</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="e6b8f-218">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-219">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-220"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="e6b8f-221">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-222"><strong>Zdanitelný dovozní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-223">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-224">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="e6b8f-225">e</span><span class="sxs-lookup"><span data-stu-id="e6b8f-225">e</span></span><li><span data-ttu-id="e6b8f-226"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="e6b8f-227">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-228"><strong>Protiúčet zdanitelných dovozních dobropisů</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="e6b8f-229">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-230">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-231">Směr daně je <strong>Importní DPH</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="e6b8f-232">d</span><span class="sxs-lookup"><span data-stu-id="e6b8f-232">d</span></span><li><span data-ttu-id="e6b8f-233">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6b8f-234"><strong>Importní DPH</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="e6b8f-235">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-236">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-237"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="e6b8f-238">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6b8f-239"><strong>Zapsat importní DPH na protiúčet</strong></span><span class="sxs-lookup"><span data-stu-id="e6b8f-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="e6b8f-240">Stornovaný součet <strong>Částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="e6b8f-241">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="e6b8f-242"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="e6b8f-243">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="e6b8f-244">Pro výše uvedenou tabulku se předpokládá, že jsou splněna tato kritéria:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="e6b8f-245">Částka základu daně je částka transakce z pole **Původ v zúčtovací měně**.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="e6b8f-246">Částka základu daně je částka transakce z pole **Částka daně skutečných prodejů**.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="e6b8f-247">Konfigurace modelu ER a formátu výkazu</span><span class="sxs-lookup"><span data-stu-id="e6b8f-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="e6b8f-248">Elektronické hlášení (ER) můžete použít ke konfiguraci výkazů a sestav a k exportu různých formátů elektronických dat bez nutnosti změny kódu X ++.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="e6b8f-249">Další informace:</span><span class="sxs-lookup"><span data-stu-id="e6b8f-249">For additional information:</span></span>

-   [<span data-ttu-id="e6b8f-250">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="e6b8f-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="e6b8f-251">Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="e6b8f-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="e6b8f-252">Požadavky na lokalizaci – vytvoření konfigurace GER</span><span class="sxs-lookup"><span data-stu-id="e6b8f-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="e6b8f-253">Prostředky pro výkazy DPH specifické podle zemí</span><span class="sxs-lookup"><span data-stu-id="e6b8f-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="e6b8f-254">Výkaz DPH pro každou zemi musí splňovat požadavky právních předpisů této země.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="e6b8f-255">Existují předdefinované obecné modely a formáty výkazů DPH pro země uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="e6b8f-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="e6b8f-256">Země</span><span class="sxs-lookup"><span data-stu-id="e6b8f-256">Country</span></span>        | <span data-ttu-id="e6b8f-257">Doplňkové informace</span><span class="sxs-lookup"><span data-stu-id="e6b8f-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e6b8f-258">Rakousko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-258">Austria</span></span>        |  [<span data-ttu-id="e6b8f-259">Podrobnosti výkazu DPH pro Rakousko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="e6b8f-260">Belgie</span><span class="sxs-lookup"><span data-stu-id="e6b8f-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="e6b8f-261">Česká republika</span><span class="sxs-lookup"><span data-stu-id="e6b8f-261">Czech Republic</span></span> |  [<span data-ttu-id="e6b8f-262">Podrobnosti výkazu DPH pro Českou republiku</span><span class="sxs-lookup"><span data-stu-id="e6b8f-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="e6b8f-263">Estonsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-263">Estonia</span></span>        |  [<span data-ttu-id="e6b8f-264">Podrobnosti výkazu DPH pro Estonsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="e6b8f-265">Finsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="e6b8f-266">Německo</span><span class="sxs-lookup"><span data-stu-id="e6b8f-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="e6b8f-267">Itálie</span><span class="sxs-lookup"><span data-stu-id="e6b8f-267">Italy</span></span>          | [<span data-ttu-id="e6b8f-268">Podrobnosti výkazu DPH pro Itálii</span><span class="sxs-lookup"><span data-stu-id="e6b8f-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="e6b8f-269">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-269">Latvia</span></span>         | [<span data-ttu-id="e6b8f-270">Podrobnosti výkazu DPH pro Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="e6b8f-271">Litva</span><span class="sxs-lookup"><span data-stu-id="e6b8f-271">Lithuania</span></span>      | [<span data-ttu-id="e6b8f-272">Podrobnosti výkazu DPH pro Litvu</span><span class="sxs-lookup"><span data-stu-id="e6b8f-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="e6b8f-273">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="e6b8f-274">Švédsko</span><span class="sxs-lookup"><span data-stu-id="e6b8f-274">Sweden</span></span>         |                                                                                 |






