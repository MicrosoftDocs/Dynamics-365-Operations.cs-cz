---
title: Seznam funkcí ER v kategorii seznamu
description: Toto téma obsahuje informace o funkcích seznamu, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9461d0afd75f421cf03ddefed5dac379f1369ec7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917757"
---
# <a name="list-of-er-functions-in-the-list-category"></a><span data-ttu-id="4fe05-103">Seznam funkcí ER v kategorii seznamu</span><span class="sxs-lookup"><span data-stu-id="4fe05-103">List of ER functions in the list category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fe05-104">Funkce seznamu elektronického výkaznictví (ER) lze používat k extrahování informací ze zdrojů dat a provádění operací se zdroji dat datových typů *Seznam záznamů* a *Kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="4fe05-104">Electronic reporting (ER) list functions can be used to extract information from, and perform operations on, data sources of the *Record list* and *Container (record)* data types.</span></span> <span data-ttu-id="4fe05-105">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="4fe05-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="4fe05-106">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="4fe05-106">List of supported functions</span></span>

| <span data-ttu-id="4fe05-107">Funkce</span><span class="sxs-lookup"><span data-stu-id="4fe05-107">Function</span></span> | <span data-ttu-id="4fe05-108">Popis</span><span class="sxs-lookup"><span data-stu-id="4fe05-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="4fe05-109">AllItems</span><span class="sxs-lookup"><span data-stu-id="4fe05-109">AllItems</span></span>](er-functions-list-allitems.md)                 | <span data-ttu-id="4fe05-110">Tato funkce je spuštěná jako výběr v paměti.</span><span class="sxs-lookup"><span data-stu-id="4fe05-110">This function runs as an in-memory selection.</span></span> <span data-ttu-id="4fe05-111">Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která sestává ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="4fe05-111">It returns a new flattened *Record list* value that consists of a list of records that represents all items that match the specified path.</span></span> |
| [<span data-ttu-id="4fe05-112">AllItemsQuery</span><span class="sxs-lookup"><span data-stu-id="4fe05-112">AllItemsQuery</span></span>](er-functions-list-allitemsquery.md)       | <span data-ttu-id="4fe05-113">Tato funkce je spuštěna jako připojený dotaz SQL.</span><span class="sxs-lookup"><span data-stu-id="4fe05-113">This function runs as a joined SQL query.</span></span> <span data-ttu-id="4fe05-114">Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která sestává ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě.</span><span class="sxs-lookup"><span data-stu-id="4fe05-114">It returns a new flattened *Record list* value that consists of a list of records that represents all items that match the specified path.</span></span> |
| [<span data-ttu-id="4fe05-115">Počet</span><span class="sxs-lookup"><span data-stu-id="4fe05-115">Count</span></span>](er-functions-list-count.md)                       | <span data-ttu-id="4fe05-116">Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="4fe05-116">This function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="4fe05-117">Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).</span><span class="sxs-lookup"><span data-stu-id="4fe05-117">If the list is empty, this function returns **0** (zero).</span></span> |
| [<span data-ttu-id="4fe05-118">EmptyList</span><span class="sxs-lookup"><span data-stu-id="4fe05-118">EmptyList</span></span>](er-functions-list-emptylist.md)               | <span data-ttu-id="4fe05-119">Tato funkce vrací prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.</span><span class="sxs-lookup"><span data-stu-id="4fe05-119">This function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>|
| [<span data-ttu-id="4fe05-120">Výčet</span><span class="sxs-lookup"><span data-stu-id="4fe05-120">Enumerate</span></span>](er-functions-list-enumerate.md)               | <span data-ttu-id="4fe05-121">Tato funkce vrací novou hodnotu typu *seznam záznamů*, která obsahuje výčtové záznamy zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="4fe05-121">This function returns a new *Record list* value that consists of enumerated records of the specified list.</span></span> |
| [<span data-ttu-id="4fe05-122">Filtr</span><span class="sxs-lookup"><span data-stu-id="4fe05-122">Filter</span></span>](er-functions-list-filter.md)                     | <span data-ttu-id="4fe05-123">Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* po změně dotazu, který jej filtruje podle zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="4fe05-123">This function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span> |
| [<span data-ttu-id="4fe05-124">První</span><span class="sxs-lookup"><span data-stu-id="4fe05-124">First</span></span>](er-functions-list-first.md)                       | <span data-ttu-id="4fe05-125">Tato funkce vrací první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="4fe05-125">This function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="4fe05-126">Pokud je seznam prázdný, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="4fe05-126">If the list is empty, this function throws an exception.</span></span> |
| [<span data-ttu-id="4fe05-127">FirstOrNull</span><span class="sxs-lookup"><span data-stu-id="4fe05-127">FirstOrNull</span></span>](er-functions-list-firstornull.md)           | <span data-ttu-id="4fe05-128">Tato funkce vrací první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento záznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="4fe05-128">This function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="4fe05-129">Je-li záznam prázdný, vrátí tato funkce hodnotu typu *kontejner (záznam)* s hodnotou null.</span><span class="sxs-lookup"><span data-stu-id="4fe05-129">If the record is empty, this function returns a null *Container (record)* value.</span></span> |
| [<span data-ttu-id="4fe05-130">Index</span><span class="sxs-lookup"><span data-stu-id="4fe05-130">Index</span></span>](er-functions-list-index.md)                       | <span data-ttu-id="4fe05-131">Tato funkce vrací hodnotu typu *kontejner (záznam)*, která je vybrána pomocí zadaného číselného indexu v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="4fe05-131">This function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="4fe05-132">Pokud je index mimo rozsah záznamů v zadaném seznamu, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="4fe05-132">If the index is out of range for the records in the specified list, this function throws an exception.</span></span> |
| [<span data-ttu-id="4fe05-133">IsEmpty</span><span class="sxs-lookup"><span data-stu-id="4fe05-133">IsEmpty</span></span>](er-functions-list-isempty.md)                   | <span data-ttu-id="4fe05-134">Tato funkce vrací *logickou hodnotu* **TRUE**, pokud zadaný seznam neobsahuje žádné záznamy.</span><span class="sxs-lookup"><span data-stu-id="4fe05-134">This function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="4fe05-135">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="4fe05-135">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="4fe05-136">Seznam</span><span class="sxs-lookup"><span data-stu-id="4fe05-136">List</span></span>](er-functions-list-list.md)                         | <span data-ttu-id="4fe05-137">Tato funkce vrací hodnotu typu *seznam záznamů*, která se skládá z nového seznamu záznamů vytvořeného ze zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="4fe05-137">This function returns a *Record list* value that consists of a new list that is created from the specified arguments.</span></span>|
| [<span data-ttu-id="4fe05-138">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="4fe05-138">ListOfFields</span></span>](er-functions-list-listoffields.md)         | <span data-ttu-id="4fe05-139">Tato funkce vrací hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury zadaného argumentu typu *výčet* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="4fe05-139">This function returns a *Record list* value that is created based on the structure of the specified argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="4fe05-140">ListOfFirstItem</span><span class="sxs-lookup"><span data-stu-id="4fe05-140">ListOfFirstItem</span></span>](er-functions-list-listoffirstitem.md)   | <span data-ttu-id="4fe05-141">Tato funkce vrací hodnotu typu *seznam záznamů*, která obsahuje pouze první záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="4fe05-141">This function returns a *Record list* value that consists of only the first record of the specified list.</span></span>|
| [<span data-ttu-id="4fe05-142">OrderBy</span><span class="sxs-lookup"><span data-stu-id="4fe05-142">OrderBy</span></span>](er-functions-list-orderby.md)                   | <span data-ttu-id="4fe05-143">Tato funkce vrací vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="4fe05-143">This function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="4fe05-144">Tyto argumenty lze definovat jako výrazy.</span><span class="sxs-lookup"><span data-stu-id="4fe05-144">These arguments can be defined as expressions.</span></span> |
| [<span data-ttu-id="4fe05-145">Stornovat</span><span class="sxs-lookup"><span data-stu-id="4fe05-145">Reverse</span></span>](er-functions-list-reverse.md)                   | <span data-ttu-id="4fe05-146">Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* v obráceném pořadí.</span><span class="sxs-lookup"><span data-stu-id="4fe05-146">This function returns the specified list as a *Record list* value in reversed sort order.</span></span> |
| [<span data-ttu-id="4fe05-147">Rozdělit</span><span class="sxs-lookup"><span data-stu-id="4fe05-147">Split</span></span>](er-functions-list-split.md)                       | <span data-ttu-id="4fe05-148">Tato funkce rozdělí zadaný vstupní řetězec do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="4fe05-148">This function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="4fe05-149">SplitList</span><span class="sxs-lookup"><span data-stu-id="4fe05-149">SplitList</span></span>](er-functions-list-splitlist.md)               | <span data-ttu-id="4fe05-150">Tato funkce rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů.</span><span class="sxs-lookup"><span data-stu-id="4fe05-150">This function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="4fe05-151">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="4fe05-151">It then returns the result as a new *Record list* value that consists of the batches.</span></span> |
| [<span data-ttu-id="4fe05-152">SplitListByLimit</span><span class="sxs-lookup"><span data-stu-id="4fe05-152">SplitListByLimit</span></span>](er-functions-list-splitlistbylimit.md) | <span data-ttu-id="4fe05-153">Tato funkce rozdělí zadaný seznam na nový seznam dílčích seznamů (dávek).</span><span class="sxs-lookup"><span data-stu-id="4fe05-153">This function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="4fe05-154">Počet záznamů v každé dávce se dynamicky vypočítává.</span><span class="sxs-lookup"><span data-stu-id="4fe05-154">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="4fe05-155">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="4fe05-155">The function then returns the result as a new *Record list* value that consists of the batches.</span></span> |
| [<span data-ttu-id="4fe05-156">StringJoin</span><span class="sxs-lookup"><span data-stu-id="4fe05-156">StringJoin</span></span>](er-functions-list-stringjoin.md)             | <span data-ttu-id="4fe05-157">Tato funkce vrací hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="4fe05-157">This function returns a *String* value that consists of concatenated values of the specified field from the specified list.</span></span> <span data-ttu-id="4fe05-158">Hodnoty mohou být odděleny určeným oddělovačem.</span><span class="sxs-lookup"><span data-stu-id="4fe05-158">The values can be separated by the specified delimiter.</span></span> |
| [<span data-ttu-id="4fe05-159">Kde</span><span class="sxs-lookup"><span data-stu-id="4fe05-159">Where</span></span>](er-functions-list-where.md)                       | <span data-ttu-id="4fe05-160">Tato funkce vrací zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl filtrován podle zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="4fe05-160">This function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="4fe05-161">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4fe05-161">Additional resources</span></span>

[<span data-ttu-id="4fe05-162">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="4fe05-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="4fe05-163">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="4fe05-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="4fe05-164">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="4fe05-164">Electronic reporting formula language</span></span>](er-formula-language.md)