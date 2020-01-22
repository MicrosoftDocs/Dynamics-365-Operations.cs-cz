---
title: Seznam funkcí ER v kategorii Datum a čas
description: Toto téma obsahuje informace o funkcích data a času, které jsou podporovány v elektronickém výkaznictví (ER).
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916561"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="51130-103">Seznam funkcí ER v kategorii Datum a čas</span><span class="sxs-lookup"><span data-stu-id="51130-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51130-104">Funkce data a času elektronického výkaznictví lze používat k extrahování informací z hodnot data a času a k provádění operací s těmito hodnotami.</span><span class="sxs-lookup"><span data-stu-id="51130-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="51130-105">Toto téma obsahuje souhrn těchto funkcí.</span><span class="sxs-lookup"><span data-stu-id="51130-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="51130-106">Seznam podporovaných funkcí</span><span class="sxs-lookup"><span data-stu-id="51130-106">List of supported functions</span></span>

| <span data-ttu-id="51130-107">Funkce</span><span class="sxs-lookup"><span data-stu-id="51130-107">Function</span></span> | <span data-ttu-id="51130-108">Popis</span><span class="sxs-lookup"><span data-stu-id="51130-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="51130-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="51130-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="51130-110">Tato funkce vrací hodnotu *DateTime*, která představuje zadaný počet dní před nebo po zadaném počátečním datu.</span><span class="sxs-lookup"><span data-stu-id="51130-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="51130-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="51130-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="51130-112">Tato funkce vrací hodnotu typu *řetězec*, která představuje zadanou hodnotu data jako text v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="51130-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="51130-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="51130-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="51130-114">Tato funkce vrací hodnotu typu *řetězec*, která představuje zadanou hodnotu data/času jako text v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="51130-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="51130-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="51130-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="51130-116">Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="51130-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="51130-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="51130-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="51130-118">Tato funkce vrací hodnotu *DateTime*, která je převedena ze zadané hodnoty kalendářního data na hodnotu data a času v koordinovaném světovém čase (Greenwich Mean Time \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="51130-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="51130-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="51130-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="51130-120">Tato funkce vrací hodnotu typu *Datum*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané jazykové verzi.</span><span class="sxs-lookup"><span data-stu-id="51130-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="51130-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="51130-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="51130-122">Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet dní mezi 1. lednem a zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="51130-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="51130-123">Dny</span><span class="sxs-lookup"><span data-stu-id="51130-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="51130-124">Tato funkce vrací hodnotu typu *celé číslo*, která představuje počet dní mezi jedním a druhým zadaným datem.</span><span class="sxs-lookup"><span data-stu-id="51130-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="51130-125">Now</span><span class="sxs-lookup"><span data-stu-id="51130-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="51130-126">Tato funkce vrací hodnotu *DateTime*, která představuje aktuální datum a čas aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="51130-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="51130-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="51130-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="51130-128">Tato funkce vrací hodnotu typu *datum*, která představuje datum typu **null** (1. leden 1900).</span><span class="sxs-lookup"><span data-stu-id="51130-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="51130-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="51130-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="51130-130">Tato funkce vrací hodnotu *DateTime*, která představuje hodnotu **null** data a času (1. leden 1900) v koordinovaném univerzálním čase (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="51130-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="51130-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="51130-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="51130-132">Tato funkce vrací hodnotu *DateTime*, která představuje aktuální datum a čas relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="51130-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="51130-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="51130-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="51130-134">Tato funkce vrací hodnotu typu *datum*, která představuje aktuální datum relace aplikace.</span><span class="sxs-lookup"><span data-stu-id="51130-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="51130-135">Dnes</span><span class="sxs-lookup"><span data-stu-id="51130-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="51130-136">Tato funkce vrací hodnotu typu *datum*, která představuje aktuální datum aplikačního serveru.</span><span class="sxs-lookup"><span data-stu-id="51130-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="51130-137">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="51130-137">Additional resources</span></span>

[<span data-ttu-id="51130-138">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="51130-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="51130-139">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="51130-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="51130-140">Jazyk receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="51130-140">Electronic reporting formula language</span></span>](er-formula-language.md)
