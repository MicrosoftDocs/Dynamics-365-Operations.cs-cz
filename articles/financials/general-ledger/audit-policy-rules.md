---
title: "Pravidla zásad auditu"
description: "Zásady auditu můžete použit pro vyhodnocení sestav výdajů, faktur dodavatele a nákupních objednávek, abyste se ujistili, že jsou v souladu s pravidly zásad, které jste vytvořili. Všechna pravidla, která jsou přidružena k zásadě auditu, jsou spouštěna v dávkovém režimu podle určeného plánu.  Každé pravidlo zásad je instancí typu pravidla zásad. Pro každý typ pravidla zásad může být aktivní pouze jedno pravidlo zásad současně."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6bebe9ce83c4b979ffbb7c86ef67ad03a650e0c2
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="audit-policy-rules"></a><span data-ttu-id="98ae2-106">Pravidla zásad auditu</span><span class="sxs-lookup"><span data-stu-id="98ae2-106">Audit policy rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98ae2-107">Zásady auditu můžete použit pro vyhodnocení sestav výdajů, faktur dodavatele a nákupních objednávek, abyste se ujistili, že jsou v souladu s pravidly zásad, které jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="98ae2-107">You can use audit policies to evaluate expense reports, vendor invoices, and purchase orders to make sure that they comply with policy rules that you create.</span></span> <span data-ttu-id="98ae2-108">Všechna pravidla, která jsou přidružena k zásadě auditu, jsou spouštěna v dávkovém režimu podle určeného plánu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-108">All of the rules that are associated with an audit policy are run in batch mode, according to a schedule that you specify.</span></span>  <span data-ttu-id="98ae2-109">Každé pravidlo zásad je instancí typu pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="98ae2-109">Each policy rule is an instance of a policy rule type.</span></span> <span data-ttu-id="98ae2-110">Pro každý typ pravidla zásad může být aktivní pouze jedno pravidlo zásad současně.</span><span class="sxs-lookup"><span data-stu-id="98ae2-110">For each policy rule type, only one policy rule can be active at a time.</span></span> 

<a name="queries-and-query-types"></a><span data-ttu-id="98ae2-111">Dotazy a typy dotazů</span><span class="sxs-lookup"><span data-stu-id="98ae2-111">Queries and query types</span></span>
-----------------------

<span data-ttu-id="98ae2-112">Když vytvoříte pravidlo zásad auditu, nejprve vyberte typ pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="98ae2-112">When you create an audit policy rule, you first select a policy rule type.</span></span> <span data-ttu-id="98ae2-113">Typ pravidla zásad určuje dotaz pro strom aplikačních objektů (AOT), který bude použit jako výchozí bod při vytvoření pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="98ae2-113">The policy rule type specifies the Application Object Tree (AOT) query to use as the starting point for creating the policy rule.</span></span> <span data-ttu-id="98ae2-114">Určuje také typ dotazu pro pravidla zásad.</span><span class="sxs-lookup"><span data-stu-id="98ae2-114">It also specifies the query type to use for the policy rule.</span></span> <span data-ttu-id="98ae2-115">Dotaz určuje zdrojový dokument, pro který je pravidlo zásad vyhodnoceno.</span><span class="sxs-lookup"><span data-stu-id="98ae2-115">The query determines the source document that the policy rule evaluates.</span></span> <span data-ttu-id="98ae2-116">Určuje také pole ve zdrojovém dokumentu, který určuje právnickou osobu a data použité při výběru dokumentů pro audit.</span><span class="sxs-lookup"><span data-stu-id="98ae2-116">It also specifies the fields in the source document that identify both the legal entity and the date to use when documents are selected for audit.</span></span> <span data-ttu-id="98ae2-117">Typ dotazu řídí výchozí pole na stránce s dotazy a na stránce pravidel zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-117">The query type controls the default fields in the query page and in the Audit policy rule page.</span></span> <span data-ttu-id="98ae2-118">V následující tabulce jsou uvedeny typy dotazů dostupné pro pravidla zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-118">The following table shows the query types that are available for audit policy rules.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98ae2-119">Typ dotazu</span><span class="sxs-lookup"><span data-stu-id="98ae2-119">Query type</span></span></th>
<th><span data-ttu-id="98ae2-120">Účel</span><span class="sxs-lookup"><span data-stu-id="98ae2-120">Purpose</span></span></th>
<th><span data-ttu-id="98ae2-121">Více informací</span><span class="sxs-lookup"><span data-stu-id="98ae2-121">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98ae2-122">Podmíněné</span><span class="sxs-lookup"><span data-stu-id="98ae2-122">Conditional</span></span></td>
<td><span data-ttu-id="98ae2-123">Vyhodnoťte atributy zdrojového dokumentu proti zadaným hodnotám.</span><span class="sxs-lookup"><span data-stu-id="98ae2-123">Evaluate source document attributes against specified values.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98ae2-124">Agregovat</span><span class="sxs-lookup"><span data-stu-id="98ae2-124">Aggregate</span></span></td>
<td><span data-ttu-id="98ae2-125">Vyhodnoťte více zdrojových dokumentů nebo řádků zdrojového dokumentu proti pravidlu zásad sečtením číselné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="98ae2-125">Evaluate multiple source documents or source document lines against a policy rule by aggregating numeric values.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98ae2-126">Vzorkování</span><span class="sxs-lookup"><span data-stu-id="98ae2-126">Sampling</span></span></td>
<td><span data-ttu-id="98ae2-127">Vyberte náhodně zadané procento zdrojových dokumentů pro vyhodnocení narušení zásad.</span><span class="sxs-lookup"><span data-stu-id="98ae2-127">Randomly select a specified percentage of the source documents to evaluate for policy violations.</span></span></td>
<td><span data-ttu-id="98ae2-128">Pokud vyberete tuto možnost, použijte stránku Pravidla zásad auditu a zadejte procento dokumentů, které chcete náhodně vybrat pro audit.</span><span class="sxs-lookup"><span data-stu-id="98ae2-128">When you select this option, use the Audit policy rule page to specify the percentage of documents to randomly select for audit.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98ae2-129">Duplicitní</span><span class="sxs-lookup"><span data-stu-id="98ae2-129">Duplicate</span></span></td>
<td><span data-ttu-id="98ae2-130">Vyhodnoťte zdrojové dokumenty a určete, zda obsahují duplicitní záznamy v určených polích.</span><span class="sxs-lookup"><span data-stu-id="98ae2-130">Evaluate source documents to determine whether they contain duplicate entries in specified fields.</span></span></td>
<td><span data-ttu-id="98ae2-131">Když vyberete tuto možnost, použijte stránku Pravidla zásad auditu a zadejte počet dní, které chcete přidat na začátek rozsahu dat pro výběr dokumentu při vyhodnocení duplicitních záznamů dokumentů.</span><span class="sxs-lookup"><span data-stu-id="98ae2-131">When you select this option, use the Audit policy rule page to specify the number of days to add to the start of the document selection date range when documents are evaluated for duplicate entries.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98ae2-132">Vyhledávání seznamu</span><span class="sxs-lookup"><span data-stu-id="98ae2-132">List search</span></span></td>
<td><span data-ttu-id="98ae2-133">Vyhodnocení zdrojových dokumentů pro dané entity.</span><span class="sxs-lookup"><span data-stu-id="98ae2-133">Evaluate source documents for specific entities.</span></span></td>
<td><span data-ttu-id="98ae2-134">Kořenový dokument dotazu definuje dokument, u kterého bude proveden audit.</span><span class="sxs-lookup"><span data-stu-id="98ae2-134">The root document of the query defines the document that is being audited.</span></span> <span data-ttu-id="98ae2-135">Dotaz musí být dotaz seznamu, který obsahuje odkaz na tabulku dirpartytable.</span><span class="sxs-lookup"><span data-stu-id="98ae2-135">The query must be a list query that includes a reference to the dirpartytable table.</span></span> <span data-ttu-id="98ae2-136">Tuto možnost lze použít pouze u dotazů AOT:</span><span class="sxs-lookup"><span data-stu-id="98ae2-136">This option can be used only with the following AOT queries:</span></span>
<ul>
<li><span data-ttu-id="98ae2-137"><span class="ui">AuditPolicyExpenseList</span> (zaměstnanci sledovaní v sestavě výdajů)</span><span class="sxs-lookup"><span data-stu-id="98ae2-137"><span class="ui">AuditPolicyExpenseList</span> (Expense report monitored employees)</span></span></li>
<li><span data-ttu-id="98ae2-138"><span class="ui">AuditPolicyPurchList</span> (dodavatelé sledovaní v nákupní objednávce)</span><span class="sxs-lookup"><span data-stu-id="98ae2-138"><span class="ui">AuditPolicyPurchList</span> (Purchase order monitored vendors)</span></span></li>
<li><span data-ttu-id="98ae2-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Dodavatelé sledovaní ve fakturách dodavatele)</span><span class="sxs-lookup"><span data-stu-id="98ae2-139"><span class="ui">AuditPolicyVendInvoiceList</span> (Vendor invoice monitored vendors)</span></span></li>
</ul>
<span data-ttu-id="98ae2-140">Pokud vyberete tuto možnost, zadejte sledované entity na stránce Pravidlo zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-140">When you select this option, specify the monitored entities in the Audit policy rule page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98ae2-141">Vyhledávání klíčových slov</span><span class="sxs-lookup"><span data-stu-id="98ae2-141">Keyword search</span></span></td>
<td><span data-ttu-id="98ae2-142">Vyhodnocení zdrojových dokumentů a určení toho, zda obsahují určitá slova.</span><span class="sxs-lookup"><span data-stu-id="98ae2-142">Evaluate source documents to determine whether they contain certain words.</span></span></td>
<td><span data-ttu-id="98ae2-143">Pokud vyberete tuto možnost, zadejte vyhledávaná slova na stránce Pravidlo zásad auditu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-143">When you select this option, enter the words to look for in the Audit policy rule page.</span></span> <span data-ttu-id="98ae2-144">Stránka Pravidlo zásad auditu obsahuje také volby, které vám umožňují určit tabulky a pole k vyhodnocení zadaných slov.</span><span class="sxs-lookup"><span data-stu-id="98ae2-144">The Audit policy rule page also includes options that let you specify the tables and fields to evaluate for the words you entered.</span></span></td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a><span data-ttu-id="98ae2-145">Společné parametry</span><span class="sxs-lookup"><span data-stu-id="98ae2-145">Common parameters</span></span>
<span data-ttu-id="98ae2-146">Všechna pravidla zásad pro určitou zásadu auditu sdílí stejné parametry dávky a stejný rozsah data pro výběr dokumentu.</span><span class="sxs-lookup"><span data-stu-id="98ae2-146">All of the policy rules for a particular audit policy share the same batch parameters and the same document selection date range.</span></span> <span data-ttu-id="98ae2-147">Tyto parametry jsou zadány pro zásady na stránce Další možnosti.</span><span class="sxs-lookup"><span data-stu-id="98ae2-147">These parameters are specified for the policy in the Additional options page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="98ae2-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="98ae2-148">Additional resources</span></span>
--------

<span data-ttu-id="98ae2-149">[Porušení a případy zásad auditu](audit-policy-violations-cases.md)
[Definování zásad auditu pro zdrojové dokumenty](tasks/define-audit-policies-source-documents.md)</span><span class="sxs-lookup"><span data-stu-id="98ae2-149">[Audit policy violations and cases](audit-policy-violations-cases.md)
[Define audit policies for source documents](tasks/define-audit-policies-source-documents.md)</span></span>



