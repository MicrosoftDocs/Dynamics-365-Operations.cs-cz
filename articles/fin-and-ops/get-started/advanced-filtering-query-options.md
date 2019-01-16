---
title: "Syntax pokročilého filtrování a dotazů"
description: "Tento článek popisuje možnosti filtrování a dotazů, které jsou k dispozici při použití dialogového okna Rozšířený filtr či řazení nebo operátoru shody v podokně filtru nebo filtrech záhlaví sloupce mřížky."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 01a508e97721099f92b9167dfdfa1b9669b9341c
ms.contentlocale: cs-cz
ms.lasthandoff: 12/18/2018

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="a00a6-103">Pokročilé filtrování a syntaxe dotazu</span><span class="sxs-lookup"><span data-stu-id="a00a6-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a00a6-104">Tento článek popisuje možnosti filtrování a dotazů, které jsou k dispozici při použití dialogového okna Rozšířený filtr či řazení nebo operátoru **shody** v podokně filtru nebo filtrech záhlaví sloupce mřížky.</span><span class="sxs-lookup"><span data-stu-id="a00a6-104">This article describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="a00a6-105">Syntax pokročilých dotazů</span><span class="sxs-lookup"><span data-stu-id="a00a6-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a00a6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a00a6-106">Syntax</span></span></th>
<th><span data-ttu-id="a00a6-107">Popis znaku</span><span class="sxs-lookup"><span data-stu-id="a00a6-107">Character description</span></span></th>
<th><span data-ttu-id="a00a6-108">popis</span><span class="sxs-lookup"><span data-stu-id="a00a6-108">Description</span></span></th>
<th><span data-ttu-id="a00a6-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="a00a6-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a00a6-110"><em>hodnota</em></span><span class="sxs-lookup"><span data-stu-id="a00a6-110"><em>value</em></span></span></td>
<td><span data-ttu-id="a00a6-111">Rovno zadané hodnotě</span><span class="sxs-lookup"><span data-stu-id="a00a6-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-112">Zadejte hodnotu, kterou chcete vyhledat.</span><span class="sxs-lookup"><span data-stu-id="a00a6-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="a00a6-113"><strong>Smith</strong> vyhledá &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-114">!<em>hodnota</em> (vykřičník)</span><span class="sxs-lookup"><span data-stu-id="a00a6-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="a00a6-115">Není rovno zadané hodnotě</span><span class="sxs-lookup"><span data-stu-id="a00a6-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-116">Před hodnotu, kterou chcete vyloučit, zadejte vykřičník.</span><span class="sxs-lookup"><span data-stu-id="a00a6-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="a00a6-117"><strong>!Smith</strong> vyhledá všechny hodnoty kromě hodnoty &quot;Smith&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-118"><em>hodnota od</em>..<em>hodnota do</em> (dvojí období)</span><span class="sxs-lookup"><span data-stu-id="a00a6-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="a00a6-119">Mezi dvěma zadanými hodnotami oddělenými dvěma tečkami</span><span class="sxs-lookup"><span data-stu-id="a00a6-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="a00a6-120">Zadejte hodnotu Od, pak dvě tečky a nakonec hodnotu Do.</span><span class="sxs-lookup"><span data-stu-id="a00a6-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="a00a6-121"><strong>1..10</strong> vyhledá všechny hodnoty od 1 do 10.</span><span class="sxs-lookup"><span data-stu-id="a00a6-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="a00a6-122">V poli řetězce však zadání hodnot <strong>A..C</strong> vyhledá všechny hodnoty, které začínají písmeny &quot;A&quot; a &quot;B&quot; a hodnoty, které se přesně rovnají &quot;C&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="a00a6-123">Tento dotaz nebude hledat například &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="a00a6-124">Chcete-li vyhledat všechny hodnoty od &quot;A<em>&quot; do &quot;C</em>&quot;, <strong>A..D</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-125">..<em>hodnota</em> (dvojí období)</span><span class="sxs-lookup"><span data-stu-id="a00a6-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="a00a6-126">Méně nebo rovno zadané hodnotě</span><span class="sxs-lookup"><span data-stu-id="a00a6-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-127">Zadejte dvě tečky a pak hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="a00a6-128"><strong>..1000</strong> vyhledá libovolné číslo menší nebo rovné hodnotě 1000: například &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-129"><em>hodnota</em>..</span><span class="sxs-lookup"><span data-stu-id="a00a6-129"><em>value</em>..</span></span> <span data-ttu-id="a00a6-130">(dvě tečky)</span><span class="sxs-lookup"><span data-stu-id="a00a6-130">(double period)</span></span></td>
<td><span data-ttu-id="a00a6-131">Větší nebo rovno zadané hodnotě</span><span class="sxs-lookup"><span data-stu-id="a00a6-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-132">Zadejte hodnotu a poté dvě tečky.</span><span class="sxs-lookup"><span data-stu-id="a00a6-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="a00a6-133"><strong>1000..</strong></span><span class="sxs-lookup"><span data-stu-id="a00a6-133"><strong>1000..</strong></span></span> <span data-ttu-id="a00a6-134">vyhledá libovolné číslo větší nebo rovné hodnotě 1000: například &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-135">&gt;<em>hodnota</em> (znaménko větší než)</span><span class="sxs-lookup"><span data-stu-id="a00a6-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="a00a6-136">Větší než zadaná hodnota</span><span class="sxs-lookup"><span data-stu-id="a00a6-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-137">Zadejte znaménko „větší než“ (<strong>&gt;</strong>) a pak hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a00a6-138"><strong>&gt;1000</strong> vyhledá libovolné číslo větší než hodnota 1000: &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-139">&lt;<em>hodnota</em> (znaménko menší než)</span><span class="sxs-lookup"><span data-stu-id="a00a6-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="a00a6-140">Menší než zadaná hodnota</span><span class="sxs-lookup"><span data-stu-id="a00a6-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-141">Zadejte znaménko „menší než“ (<strong>&lt;</strong>) a pak hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="a00a6-142"><strong>&lt;1000</strong> vyhledá libovolné číslo menší než hodnota 1000: například &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-143"><em>hodnota</em>\* (hvězdička)</span><span class="sxs-lookup"><span data-stu-id="a00a6-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="a00a6-144">Začínající od zadané hodnoty</span><span class="sxs-lookup"><span data-stu-id="a00a6-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-145">Zadejte počáteční hodnotu a pak hvězdičku (<strong>\*</strong>).</span><span class="sxs-lookup"><span data-stu-id="a00a6-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="a00a6-146"><strong>S\*</strong>nalezne libovolný řetězec začínající na &quot;S&quot;, jako například &quot;Stockholm&quot;, &quot;Sydney&quot;, a &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-147">\*<em>hodnota</em> (hvězdička)</span><span class="sxs-lookup"><span data-stu-id="a00a6-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="a00a6-148">Končí zadanou hodnotou</span><span class="sxs-lookup"><span data-stu-id="a00a6-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-149">Zadejte hvězdičku a pak konečnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="a00a6-150"><strong>\*east</strong>nalezne řetězec končící na &quot;východ&quot;, jako například &quot;severovýchod&quot; nebo &quot;jihovýchod&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-151">*<em>hodnota</em>* (hvězdička)</span><span class="sxs-lookup"><span data-stu-id="a00a6-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="a00a6-152">Obsahující zadanou hodnotu</span><span class="sxs-lookup"><span data-stu-id="a00a6-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="a00a6-153">Zadejte hvězdičku, pak hodnotu, a nakonec opět hvězdičku.</span><span class="sxs-lookup"><span data-stu-id="a00a6-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="a00a6-154"><strong>*th*</strong> nalezne libovolný řetězec obsahující &quot;ch&quot;, jako například &quot;severovýchod&quot; nebo &quot;jihovýchod&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-155">?</span><span class="sxs-lookup"><span data-stu-id="a00a6-155">?</span></span> <span data-ttu-id="a00a6-156">(otazník)</span><span class="sxs-lookup"><span data-stu-id="a00a6-156">(question mark)</span></span></td>
<td><span data-ttu-id="a00a6-157">Obsahující jeden nebo více neznámých znaků</span><span class="sxs-lookup"><span data-stu-id="a00a6-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="a00a6-158">V pozici neznámého znaku v hodnotě můžete zadat otazník.</span><span class="sxs-lookup"><span data-stu-id="a00a6-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="a00a6-159"><strong>Sm?th</strong> nalezne &quot;Smith&quot; a &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-160"><em>hodnota</em>,<em>hodnota</em> (čárka)</span><span class="sxs-lookup"><span data-stu-id="a00a6-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="a00a6-161">Shoduje se s hodnotami oddělenými čárkou</span><span class="sxs-lookup"><span data-stu-id="a00a6-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="a00a6-162">Zadejte veškerá vaše kritéria a oddělte je čárkami.</span><span class="sxs-lookup"><span data-stu-id="a00a6-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="a00a6-163"><strong>A, D, F, G</strong> vyhledá přesně &quot;A&quot;, &quot;D&quot;, &quot;F&quot; a &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="a00a6-164"><strong>10, 20, 30, 100</strong> vyhledá přesně &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="a00a6-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-165">(<span class="code">příkaz SQL</span>) (příkaz SQL v uvozovkách)</span><span class="sxs-lookup"><span data-stu-id="a00a6-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="a00a6-166">Nalezení definovaného dotazu</span><span class="sxs-lookup"><span data-stu-id="a00a6-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="a00a6-167">Zadejte dotaz ve formě příkazu SQL v uvozovkách.</span><span class="sxs-lookup"><span data-stu-id="a00a6-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="a00a6-168"><strong><span class="code">(datový zdroj.Název pole != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="a00a6-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-169">bil.</span><span class="sxs-lookup"><span data-stu-id="a00a6-169">T</span></span></td>
<td><span data-ttu-id="a00a6-170">Dnešní datum</span><span class="sxs-lookup"><span data-stu-id="a00a6-170">Today's date</span></span></td>
<td><span data-ttu-id="a00a6-171">Zadejte <strong>T</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="a00a6-172"><strong>T</strong> odpovídá dnešnímu datu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-173">(methodName(parameters)) (metoda <strong>SysQueryRangeUtil</strong> v uvozovkách)</span><span class="sxs-lookup"><span data-stu-id="a00a6-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="a00a6-174">Párování hodnoty nebo rozsahu hodnot zadaných za pomoci parametrů metody <strong>SysQueryRangeUtil</strong></span><span class="sxs-lookup"><span data-stu-id="a00a6-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="a00a6-175">Zadejte parametry metody <strong>SysQueryRangeUtil</strong> Párování pro určení hodnoty nebo rozsahu hodnot.</span><span class="sxs-lookup"><span data-stu-id="a00a6-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="a00a6-176">Klikněte na <strong>Pohledávky</strong> &gt; <strong>Faktury</strong> &gt; <strong>Otevřené faktury odběratele</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-177">Stisknutím kombinace kláves Ctrl + Shift + F3 otevřete stránku <strong>Dotaz</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="a00a6-178">Na kartě <strong>Rozsah</strong> klepněte na možnost <strong>Přidat</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-179">V poli <strong>Tabulka</strong> vyberte <strong>Otevřít transakce odběratelů</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-180">V poli <strong>Pole</strong> vyberte <strong>Datum splatnosti</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-181">V poli <strong>Kritéria</strong> zadejte <strong>(yearRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-182">Klepněte na tlačítko <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="a00a6-183">Stránka seznamu se aktualizuje a bude obsahovat seznam faktur, které odpovídají zadaným kritériím.</span><span class="sxs-lookup"><span data-stu-id="a00a6-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="a00a6-184">V tomto případě budou uvedeny faktury, které byly splatné v předchozích dvou letech.</span><span class="sxs-lookup"><span data-stu-id="a00a6-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="a00a6-185">Další podrobnosti o metodách pro data <strong>SysQueryRangeUtil</strong> a několik příkladů naleznete v tabulce v další části.</span><span class="sxs-lookup"><span data-stu-id="a00a6-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="a00a6-186">Upřesnění datových dotazů, které používají metody SysQueryRangeUtil</span><span class="sxs-lookup"><span data-stu-id="a00a6-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a00a6-187">Metoda</span><span class="sxs-lookup"><span data-stu-id="a00a6-187">Method</span></span></th>
<th><span data-ttu-id="a00a6-188">Popis</span><span class="sxs-lookup"><span data-stu-id="a00a6-188">Description</span></span></th>
<th><span data-ttu-id="a00a6-189">Příklad</span><span class="sxs-lookup"><span data-stu-id="a00a6-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a00a6-190">Den (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a00a6-191">Vyhledání data vzhledem k datu relace.</span><span class="sxs-lookup"><span data-stu-id="a00a6-191">Find a date relative to the session date.</span></span> <span data-ttu-id="a00a6-192">Kladné hodnoty naznačují budoucí data a záporné hodnoty dřívější data.</span><span class="sxs-lookup"><span data-stu-id="a00a6-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-193"><strong>Zítra</strong> – zadejte <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-194"><strong>Dnes</strong> – zadejte <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-195"><strong>Včera</strong> – zadejte <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="a00a6-197">Vyhledání rozsahu vzhledem k datu relace.</span><span class="sxs-lookup"><span data-stu-id="a00a6-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="a00a6-198">Kladné hodnoty naznačují budoucí data a záporné hodnoty dřívější data.</span><span class="sxs-lookup"><span data-stu-id="a00a6-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-199"><strong>Posledních 30 dnů</strong> – zadejte <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-200"><strong>Posledních 30 dnů a budoucích 30 dnů</strong> – zadejte <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a00a6-202">Vyhledání všech dat po určeném relativním datu.</span><span class="sxs-lookup"><span data-stu-id="a00a6-202">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-203"><strong>Více než 30 dnů ode dneška</strong> – zadejte <strong>(GreaterThanDate(30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a00a6-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a00a6-205">Vyhledání všech záznamů data/času po aktuálním času.</span><span class="sxs-lookup"><span data-stu-id="a00a6-205">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-206"><strong>Všechna budoucí data a časy</strong> – zadejte <strong>(GreaterThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="a00a6-208">Vyhledání všech dat před určeném relativním datem.</span><span class="sxs-lookup"><span data-stu-id="a00a6-208">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-209"><strong>Méně než sedm dní ode dneška</strong> – zadejte <strong>(LessThanDate(7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="a00a6-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="a00a6-211">Vyhledání všech záznamů data/času před aktuálním časem.</span><span class="sxs-lookup"><span data-stu-id="a00a6-211">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-212"><strong>Všechna minulá data/časy</strong> – zadejte <strong>(LessThanUtcNow())</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a00a6-214">Vyhledání rozsahu dat na základě měsíců vzhledem k aktuálnímu měsíci.</span><span class="sxs-lookup"><span data-stu-id="a00a6-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-215"><strong>Předchozí dva měsíce</strong> – zadejte <strong>(MonthRange(-2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-216"><strong>Následující tři měsíce</strong> – zadejte <strong>(MonthRange(0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a00a6-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="a00a6-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="a00a6-218">Vyhledání rozsahu dat na základě roků vzhledem k aktuálnímu roku.</span><span class="sxs-lookup"><span data-stu-id="a00a6-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a00a6-219"><strong>Příští rok</strong> – zadejte <strong>(YearRange(0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="a00a6-220"><strong>Předchozí rok</strong> – zadejte <strong>(YearRange(-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="a00a6-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

