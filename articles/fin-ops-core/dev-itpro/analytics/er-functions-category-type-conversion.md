---
title: Seznam funkcí ER v kategorii převodu typu
description: Toto téma obsahuje informace o funkcích převodu, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 199d51ae8a4dbdd7d2f3bd290a2b487ceb1174dc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752597"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="dfaf6-103">Seznam funkcí ER v kategorii převodu typu</span><span class="sxs-lookup"><span data-stu-id="dfaf6-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfaf6-104">K převodu hodnot mezi typy lze použít funkce pro převod typů elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="dfaf6-105">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="dfaf6-106">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="dfaf6-106">Type conversion functions</span></span>

| <span data-ttu-id="dfaf6-107">Funkce</span><span class="sxs-lookup"><span data-stu-id="dfaf6-107">Function</span></span> | <span data-ttu-id="dfaf6-108">Popis</span><span class="sxs-lookup"><span data-stu-id="dfaf6-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="dfaf6-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="dfaf6-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="dfaf6-110">Tato funkce vrací hodnotu *Int64*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="dfaf6-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="dfaf6-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="dfaf6-112">Tato funkce vrací hodnotu *Int*, která představuje zadaný řetězec.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="dfaf6-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="dfaf6-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="dfaf6-114">Tato funkce vrací hodnotu typu *reálné číslo*, která je převedena ze zadané hodnoty typu *Řetězec*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="dfaf6-115">Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="dfaf6-116">Hodnota</span><span class="sxs-lookup"><span data-stu-id="dfaf6-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="dfaf6-117">Tato funkce vrací hodnotu typu *reálné číslo*, která je převedena ze zadané hodnoty typu *Řetězec*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="dfaf6-118">Funkce převodu typu v kategorii kontejneru</span><span class="sxs-lookup"><span data-stu-id="dfaf6-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="dfaf6-119">V následující tabulce jsou popsány funkce pro převod typů v kategorii [kontejner](er-functions-category-container.md).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="dfaf6-120">Funkce</span><span class="sxs-lookup"><span data-stu-id="dfaf6-120">Function</span></span> | <span data-ttu-id="dfaf6-121">popis</span><span class="sxs-lookup"><span data-stu-id="dfaf6-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="dfaf6-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="dfaf6-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="dfaf6-123">Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *Kontejner*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="dfaf6-124">Funkce převodu typu v kategorii datum a čas</span><span class="sxs-lookup"><span data-stu-id="dfaf6-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="dfaf6-125">V následující tabulce jsou popsány funkce pro převod typů v [kategorii datum a čas](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="dfaf6-126">Funkce</span><span class="sxs-lookup"><span data-stu-id="dfaf6-126">Function</span></span> | <span data-ttu-id="dfaf6-127">Popis</span><span class="sxs-lookup"><span data-stu-id="dfaf6-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="dfaf6-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="dfaf6-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="dfaf6-129">Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty typu *řetězec* v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="dfaf6-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="dfaf6-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="dfaf6-131">Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty *datum* na hodnotu data a času v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="dfaf6-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="dfaf6-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="dfaf6-133">Tato funkce vrací hodnotu *Datum*, která je převedena ze zadané hodnoty typu *řetězec* v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="dfaf6-134">Funkce převodu typu v kategorii seznamu</span><span class="sxs-lookup"><span data-stu-id="dfaf6-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="dfaf6-135">V následující tabulce jsou popsány funkce pro převod typů v [kategorii seznamu](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="dfaf6-136">Funkce</span><span class="sxs-lookup"><span data-stu-id="dfaf6-136">Function</span></span> | <span data-ttu-id="dfaf6-137">Popis</span><span class="sxs-lookup"><span data-stu-id="dfaf6-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="dfaf6-138">Seznam</span><span class="sxs-lookup"><span data-stu-id="dfaf6-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="dfaf6-139">Tato funkce vrací hodnotu *seznam záznamů*, která je vytvořena ze specifikovaných argumentů typu *Kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="dfaf6-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="dfaf6-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="dfaf6-141">Tato funkce vrací hodnotu typu *seznam záznamů*, která je vytvořena na základě struktury daného argumentu typu *výčet* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="dfaf6-142">Rozdělit</span><span class="sxs-lookup"><span data-stu-id="dfaf6-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="dfaf6-143">Tato funkce rozdělí zadanou hodnotu *řetězec* do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="dfaf6-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="dfaf6-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="dfaf6-145">Tato funkce vrací hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadané hodnoty *Seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="dfaf6-146">Hodnoty mohou být odděleny určeným oddělovačem.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="dfaf6-147">Funkce převodu typu v textové kategorii</span><span class="sxs-lookup"><span data-stu-id="dfaf6-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="dfaf6-148">V následující tabulce jsou popsány funkce pro převod typů v [kategorii textu](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="dfaf6-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="dfaf6-149">Funkce</span><span class="sxs-lookup"><span data-stu-id="dfaf6-149">Function</span></span> | <span data-ttu-id="dfaf6-150">Popis</span><span class="sxs-lookup"><span data-stu-id="dfaf6-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="dfaf6-151">Char</span><span class="sxs-lookup"><span data-stu-id="dfaf6-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="dfaf6-152">Tato funkce vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="dfaf6-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="dfaf6-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="dfaf6-154">Tato funkce převede zadaný vstup datového typu *String* na datovou položku datového typu *GUID*.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="dfaf6-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="dfaf6-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="dfaf6-156">Tato funkce vrací hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="dfaf6-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="dfaf6-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="dfaf6-158">Tato funkce vrací hodnotu *kontejner*, která zobrazuje kód rychlé odpovědi (QR kód) pro zadaný řetězec v binárním formátu.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="dfaf6-159">Text</span><span class="sxs-lookup"><span data-stu-id="dfaf6-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="dfaf6-160">Tato funkce vrací hodnotu *řetězec*, která představuje zadané číslo poté, co bylo převedeno na textový řetězec formátovaný podle nastavení národního prostředí jazyka stávající instance aplikace.</span><span class="sxs-lookup"><span data-stu-id="dfaf6-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="dfaf6-161">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="dfaf6-161">Additional resources</span></span>

[<span data-ttu-id="dfaf6-162">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="dfaf6-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="dfaf6-163">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="dfaf6-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="dfaf6-164">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="dfaf6-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]