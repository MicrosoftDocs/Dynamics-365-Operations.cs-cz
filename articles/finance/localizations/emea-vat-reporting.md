---
title: Vykazování DPH pro Evropu
description: Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 444726e6295fb127316af9c8382ccb4d25d28ce3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232000"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="b7400-103">Vykazování DPH pro Evropu</span><span class="sxs-lookup"><span data-stu-id="b7400-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7400-104">Toto téma obsahuje obecné informace o nastavení a generování výkazu daně z přidané hodnoty (DPH) pro některé evropské země.</span><span class="sxs-lookup"><span data-stu-id="b7400-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="b7400-105">Toto téma obsahuje obecný přístup k nastavení a generování výkazu DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="b7400-106">Tento přístup je společný pro uživatele v právnických osobách v těchto zemích a oblastech:</span><span class="sxs-lookup"><span data-stu-id="b7400-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="b7400-107">Rakousko</span><span class="sxs-lookup"><span data-stu-id="b7400-107">Austria</span></span>
-   <span data-ttu-id="b7400-108">Belgie</span><span class="sxs-lookup"><span data-stu-id="b7400-108">Belgium</span></span>
-   <span data-ttu-id="b7400-109">Česká republika</span><span class="sxs-lookup"><span data-stu-id="b7400-109">Czech Republic</span></span>
-   <span data-ttu-id="b7400-110">Estonsko</span><span class="sxs-lookup"><span data-stu-id="b7400-110">Estonia</span></span>
-   <span data-ttu-id="b7400-111">Finsko</span><span class="sxs-lookup"><span data-stu-id="b7400-111">Finland</span></span>
-   <span data-ttu-id="b7400-112">Německo</span><span class="sxs-lookup"><span data-stu-id="b7400-112">Germany</span></span>
-   <span data-ttu-id="b7400-113">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="b7400-113">Latvia</span></span>
-   <span data-ttu-id="b7400-114">Litva</span><span class="sxs-lookup"><span data-stu-id="b7400-114">Lithuania</span></span>
-   <span data-ttu-id="b7400-115">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="b7400-115">Netherlands</span></span>
-   <span data-ttu-id="b7400-116">Švédsko</span><span class="sxs-lookup"><span data-stu-id="b7400-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="b7400-117">Přehled výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="b7400-117">VAT statement overview</span></span>
<span data-ttu-id="b7400-118">Výkaz DPH je založený na částkách daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="b7400-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="b7400-119">Proces generování výkazu DPH je součástí procesu platby DPH, který je implementován pomocí funkce vypořádání a zaúčtování DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="b7400-120">Tato funkce se používá k výpočtu DPH splatné pro dané období.</span><span class="sxs-lookup"><span data-stu-id="b7400-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="b7400-121">Výpočet vyrovnání zahrnuje zaúčtovanou DPH pro vybrané období vyrovnání daňových transakcí.</span><span class="sxs-lookup"><span data-stu-id="b7400-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="b7400-122">Postup pro výpočet dat pro výkaz DPH je založen na vztahu mezi kódy DPH a kódy vykazování DPH, kde kódy vykazování daně odpovídají polím s výkazy DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="b7400-123">Pro každý kód DPH by měly být nastaveny kódy vykazování DPH pro každý typ transakce, například zdanitelné prodeje zdanitelné nákupy, zdanitelný import.</span><span class="sxs-lookup"><span data-stu-id="b7400-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="b7400-124">Tento typ transakcí je popsán v části Kódy DPH pro vykazování DPH dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="b7400-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="b7400-125">Pro každý kód vykazování by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="b7400-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="b7400-126">Ve stejnou dobu jsou kódy DPH propojeny s konkrétním finančním úřadem prostřednictvím období vyrovnání DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="b7400-127">Pro každý finanční úřad pro vykazování DPH by mělo být určeno konkrétní rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="b7400-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="b7400-128">Tedy pouze kódy vykazování DPH se stejným rozložením sestavy, která je nastavena pro finanční úřad k odvedení DPH v období vyrovnání DPH pro kód DPH lze vybrat v nastavení sestavy kódu DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="b7400-129">Transakce DPH generované při účtování objednávky nebo deníku obsahují kód DPH, zdroj DPH, směr DPH a částky transakcí (částka základu daně a výše daně v zúčtovací měně, měně DPH a měně transakce).</span><span class="sxs-lookup"><span data-stu-id="b7400-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="b7400-130">V závislosti na kombinaci atributů transakce DPH, částky transakce tvoří celkové částky určené pro kódy vykazování DPH určené pro kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="b7400-131">Následující obrázek znázorňuje vztah mezi daty.</span><span class="sxs-lookup"><span data-stu-id="b7400-131">The following illustration shows the data relationship.</span></span>

![diagram](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="b7400-133">Nastavení výkazu DPH</span><span class="sxs-lookup"><span data-stu-id="b7400-133">VAT statement setup</span></span>
<span data-ttu-id="b7400-134">Chcete-li generovat výkazy DPH, je nutné vytvořit následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="b7400-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="b7400-135">Nastavení daňových úřadů pro vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="b7400-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="b7400-136">Dříve než můžete vytvořit kódy vykazování DPH, je nutné vybrat správnou sestavu rozložení pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="b7400-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="b7400-137">Na stránce **Finanční úřady** v části **Obecné** vyberte **Rozložení sestavy**.</span><span class="sxs-lookup"><span data-stu-id="b7400-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="b7400-138">Toto rozložení bude použito, když nastavujete kódy vykazování DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="b7400-139">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="b7400-139">Sales tax reporting codes</span></span>

<span data-ttu-id="b7400-140">Kódy vykazování DPH jsou pole kódy DPH výkazu nebo značky názvy ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="b7400-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="b7400-141">Tyto kódy se používají k agregaci a přípravě částky v sestavě.</span><span class="sxs-lookup"><span data-stu-id="b7400-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="b7400-142">Při konfiguraci elektronického formátu vykazování ve výkazu DPH budou použity názvy částek výsledku.</span><span class="sxs-lookup"><span data-stu-id="b7400-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="b7400-143">Můžete vytvářet a udržovat kódy vykazování DPH na stránce **Kódy vykazování DPH**.</span><span class="sxs-lookup"><span data-stu-id="b7400-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="b7400-144">Každý kód je nutné přiřadit rozložení sestavy.</span><span class="sxs-lookup"><span data-stu-id="b7400-144">You must assign each code a report layout.</span></span> <span data-ttu-id="b7400-145">Jakmile vytvoříte kódy vykazování DPH, můžete použít kódy v části **Nastavení sestavy** na stránce **Kódy DPH**.</span><span class="sxs-lookup"><span data-stu-id="b7400-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="b7400-146">Kódy vykazování DPH</span><span class="sxs-lookup"><span data-stu-id="b7400-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="b7400-147"> Základní částky a daňové částky prodejní daně mohou být agregovány v kódech vykazování ve výkazu DPH (značky XML nebo deklarace polí).</span><span class="sxs-lookup"><span data-stu-id="b7400-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="b7400-148">Můžete to nastavit přiřazením vykazování kódů různých typů transakcí pro kódy DPH na DPH <strong>kódy DPH</strong> stránky.</span><span class="sxs-lookup"><span data-stu-id="b7400-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="b7400-149">Následující tabulka popisuje typy transakcí v nastavení sestavy pro kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="b7400-150">Výpočet zahrnuje transakce pro všechny typy zdrojů s výjimkou DPH.</span><span class="sxs-lookup"><span data-stu-id="b7400-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b7400-151"><strong>Typ transakce</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="b7400-152"><strong>Popis transakcí a částek pro výpočet v typu transakce</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-153"><strong>Zdanitelné prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="b7400-154">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-155">Datum transakce je ve vybraném období/</span><span class="sxs-lookup"><span data-stu-id="b7400-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="b7400-156">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-157">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-158"><strong>Prodej bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="b7400-159">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-160">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-161">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="b7400-162">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-163"><strong>DPH na výstupu</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="b7400-164">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-165">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-166">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-167">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-168"><strong>Zdanitelný prodejní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-169">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-170">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-171">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-172">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-173"><strong>Prodejní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-174">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-175">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-176">Prodej je export (<strong>směr daně</strong> je <strong>Prodej bez DPH</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="b7400-177">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-178"><strong>DPH na prodejním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-179">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-180">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-181">Prodej je domácí (<strong>směr daně</strong> je <strong>DPH na výstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-182">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-183"><strong>Zdanitelné nákupy</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="b7400-184">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-185">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-186">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-187">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-188"><strong>Nákup bez daně</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="b7400-189">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-190">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-191">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="b7400-192">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-193"><strong>DPH na vstupu</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="b7400-194">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-195">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-196">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-197">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-198"><strong>Zdanitelný nákupní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-199">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-200">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-201">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-202">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-203"><strong>Nákupní dobropis osvobozený od daně</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-204">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-205">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-206">Prodej je import (<strong>směr daně</strong> je <strong>Nákup bez daně</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="b7400-207">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-208"><strong>DPH na nákupním dobropisu</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-209">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-210">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-211">Nákup je domácí (<strong>směr daně</strong> je <strong>DPH na vstupu</strong>).</span><span class="sxs-lookup"><span data-stu-id="b7400-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b7400-212">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-213"><strong>Zdanitelný import</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="b7400-214">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-215">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-216"><strong>Směr daně</strong> je <strong>Použít daň</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="b7400-217">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-218"><strong>Protiúčet zdanitelného dovozu</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="b7400-219">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-220">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-221"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7400-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b7400-222">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-223"><strong>Zdanitelný dovozní dobropis</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-224">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-225">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="b7400-226">e</span><span class="sxs-lookup"><span data-stu-id="b7400-226">e</span></span><li><span data-ttu-id="b7400-227"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7400-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b7400-228">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-229"><strong>Protiúčet zdanitelných dovozních dobropisů</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="b7400-230">Stornovaný součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-231">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-232">Směr daně je <strong>Importní DPH</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7400-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="b7400-233">d</span><span class="sxs-lookup"><span data-stu-id="b7400-233">d</span></span><li><span data-ttu-id="b7400-234">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7400-235"><strong>Importní DPH</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="b7400-236">Součet <strong>Základních částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-237">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-238"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7400-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b7400-239">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7400-240"><strong>Zapsat importní DPH na protiúčet</strong></span><span class="sxs-lookup"><span data-stu-id="b7400-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="b7400-241">Stornovaný součet <strong>Částek daně</strong> daňových transakcí, který splňuje následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="b7400-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b7400-242">Datum transakce je ve vybraném období.</span><span class="sxs-lookup"><span data-stu-id="b7400-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b7400-243"><strong>Směr daně</strong> je <strong>Použít daň</strong>.</span><span class="sxs-lookup"><span data-stu-id="b7400-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b7400-244">Transakce <strong>částka základu daně</strong> nebo <strong>částka daně</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b7400-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b7400-245">Pro výše uvedenou tabulku se předpokládá, že jsou splněna tato kritéria:</span><span class="sxs-lookup"><span data-stu-id="b7400-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="b7400-246">Částka základu daně je částka transakce z pole **Původ v zúčtovací měně**.</span><span class="sxs-lookup"><span data-stu-id="b7400-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="b7400-247">Částka základu daně je částka transakce z pole **Částka daně skutečných prodejů**.</span><span class="sxs-lookup"><span data-stu-id="b7400-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="b7400-248">Konfigurace modelu ER a formátu výkazu</span><span class="sxs-lookup"><span data-stu-id="b7400-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="b7400-249">Elektronické hlášení (ER) můžete použít ke konfiguraci výkazů a sestav a k exportu různých formátů elektronických dat bez nutnosti změny kódu X ++.</span><span class="sxs-lookup"><span data-stu-id="b7400-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="b7400-250">Další informace:</span><span class="sxs-lookup"><span data-stu-id="b7400-250">For additional information:</span></span>

-   [<span data-ttu-id="b7400-251">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b7400-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="b7400-252">Stažení konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b7400-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="b7400-253">Požadavky na lokalizaci – vytvoření konfigurace GER</span><span class="sxs-lookup"><span data-stu-id="b7400-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="b7400-254">Prostředky pro výkazy DPH specifické podle zemí</span><span class="sxs-lookup"><span data-stu-id="b7400-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="b7400-255">Výkaz DPH pro každou zemi musí splňovat požadavky právních předpisů této země.</span><span class="sxs-lookup"><span data-stu-id="b7400-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="b7400-256">Existují předdefinované obecné modely a formáty výkazů DPH pro země uvedené v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="b7400-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="b7400-257">Země</span><span class="sxs-lookup"><span data-stu-id="b7400-257">Country</span></span>        | <span data-ttu-id="b7400-258">Doplňkové informace</span><span class="sxs-lookup"><span data-stu-id="b7400-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b7400-259">Rakousko</span><span class="sxs-lookup"><span data-stu-id="b7400-259">Austria</span></span>        |  [<span data-ttu-id="b7400-260">Podrobnosti výkazu DPH pro Rakousko</span><span class="sxs-lookup"><span data-stu-id="b7400-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="b7400-261">Belgie</span><span class="sxs-lookup"><span data-stu-id="b7400-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="b7400-262">Česká republika</span><span class="sxs-lookup"><span data-stu-id="b7400-262">Czech Republic</span></span> |  [<span data-ttu-id="b7400-263">Výkaz DPH pro Českou republiku</span><span class="sxs-lookup"><span data-stu-id="b7400-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="b7400-264">Estonsko</span><span class="sxs-lookup"><span data-stu-id="b7400-264">Estonia</span></span>        |  [<span data-ttu-id="b7400-265">Podrobnosti výkazu DPH pro Estonsko</span><span class="sxs-lookup"><span data-stu-id="b7400-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="b7400-266">Finsko</span><span class="sxs-lookup"><span data-stu-id="b7400-266">Finland</span></span>        | [<span data-ttu-id="b7400-267">Sestava DPH pro Finsko</span><span class="sxs-lookup"><span data-stu-id="b7400-267">Sales tax report for Finland</span></span>](emea-fin-sales-tax-payment-report-finland.md)          |
| <span data-ttu-id="b7400-268">Německo</span><span class="sxs-lookup"><span data-stu-id="b7400-268">Germany</span></span>        | [<span data-ttu-id="b7400-269">Přiznání k DPH pro Německo</span><span class="sxs-lookup"><span data-stu-id="b7400-269">VAT declaration for Germany</span></span>](emea-de-vat-declaration.md)                       |
| <span data-ttu-id="b7400-270">Itálie</span><span class="sxs-lookup"><span data-stu-id="b7400-270">Italy</span></span>          | [<span data-ttu-id="b7400-271">Podrobnosti výkazu DPH pro Itálii</span><span class="sxs-lookup"><span data-stu-id="b7400-271">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="b7400-272">Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="b7400-272">Latvia</span></span>         | [<span data-ttu-id="b7400-273">Podrobnosti výkazu DPH pro Lotyšsko</span><span class="sxs-lookup"><span data-stu-id="b7400-273">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="b7400-274">Litva</span><span class="sxs-lookup"><span data-stu-id="b7400-274">Lithuania</span></span>      | [<span data-ttu-id="b7400-275">Podrobnosti výkazu DPH pro Litvu</span><span class="sxs-lookup"><span data-stu-id="b7400-275">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="b7400-276">Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="b7400-276">Netherlands</span></span>    | [<span data-ttu-id="b7400-277">Formát přiznání k DPH pro Nizozemsko</span><span class="sxs-lookup"><span data-stu-id="b7400-277">VAT declaration for the Netherlands</span></span>](emea-nl-vat-declaration.md)           |
| <span data-ttu-id="b7400-278">Švédsko</span><span class="sxs-lookup"><span data-stu-id="b7400-278">Sweden</span></span>         | [<span data-ttu-id="b7400-279">Sestava DPH pro Švédsko</span><span class="sxs-lookup"><span data-stu-id="b7400-279">Sales tax report for Sweden</span></span>](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]