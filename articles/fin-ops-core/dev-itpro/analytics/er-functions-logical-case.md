---
title: Funkce el. výkaznictví CASE
description: Toto téma obsahuje obecné informace o použití funkce CASE elektronického výkaznictví.
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
ms.openlocfilehash: 605bd50005ee4e5866a5be9e16df6da3139ad19c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744760"
---
# <a name="case-er-function"></a><span data-ttu-id="176e4-103">Funkce el. výkaznictví CASE</span><span class="sxs-lookup"><span data-stu-id="176e4-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="176e4-104">Funkce `CASE` vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu.</span><span class="sxs-lookup"><span data-stu-id="176e4-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="176e4-105">V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost.</span><span class="sxs-lookup"><span data-stu-id="176e4-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="176e4-106">Vrácená hodnota může být libovolného podporovaného datového typu.</span><span class="sxs-lookup"><span data-stu-id="176e4-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="176e4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="176e4-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="176e4-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="176e4-108">Arguments</span></span>

<span data-ttu-id="176e4-109">`expression`: *primitivní datový typ* (logická, číselná nebo textová hodnota)</span><span class="sxs-lookup"><span data-stu-id="176e4-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="176e4-110">Platný výraz, který vrací hodnotu primitivního datového typu.</span><span class="sxs-lookup"><span data-stu-id="176e4-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="176e4-111">`option 1`: *primitivní datový typ* (logická, číselná nebo textová hodnota)</span><span class="sxs-lookup"><span data-stu-id="176e4-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="176e4-112">Platný výraz, který vrací hodnotu stejného primitivního datového typu jako argument `expression` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="176e4-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="176e4-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="176e4-113">This argument is required.</span></span>

<span data-ttu-id="176e4-114">`result 1`: *kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="176e4-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="176e4-115">Vrácený výsledek, který odpovídá předcházející možnosti.</span><span class="sxs-lookup"><span data-stu-id="176e4-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="176e4-116">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="176e4-116">This argument is required.</span></span>

<span data-ttu-id="176e4-117">`option N`: *primitivní datový typ* (logická, číselná nebo textová hodnota)</span><span class="sxs-lookup"><span data-stu-id="176e4-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="176e4-118">Platný výraz, který vrací hodnotu stejného primitivního datového typu jako argument `expression` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="176e4-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="176e4-119">Tento argument je volitelný.</span><span class="sxs-lookup"><span data-stu-id="176e4-119">This argument is optional.</span></span>

<span data-ttu-id="176e4-120">`result N`: *kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="176e4-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="176e4-121">Vrácený výsledek, který odpovídá předcházející možnosti.</span><span class="sxs-lookup"><span data-stu-id="176e4-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="176e4-122">Tento argument je volitelný.</span><span class="sxs-lookup"><span data-stu-id="176e4-122">This argument is optional.</span></span>

<span data-ttu-id="176e4-123">`default result`: *kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="176e4-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="176e4-124">Výsledek, který by měl být vrácen, pokud neexistuje shoda.</span><span class="sxs-lookup"><span data-stu-id="176e4-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="176e4-125">Tento argument je volitelný.</span><span class="sxs-lookup"><span data-stu-id="176e4-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="176e4-126">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="176e4-126">Return values</span></span>

<span data-ttu-id="176e4-127">*kterýkoli z podporovaných datových typů*</span><span class="sxs-lookup"><span data-stu-id="176e4-127">*Any of the supported data types*</span></span>

<span data-ttu-id="176e4-128">Výsledná hodnota některého z podporovaných datových typů.</span><span class="sxs-lookup"><span data-stu-id="176e4-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="176e4-129">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="176e4-129">Usage notes</span></span>

<span data-ttu-id="176e4-130">Výjimka je vyvolána za běhu, pokud neexistuje shoda a volitelný výchozí výsledek není definován.</span><span class="sxs-lookup"><span data-stu-id="176e4-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="176e4-131">Všechny výsledky musí být zadány pomocí stejného datového typu.</span><span class="sxs-lookup"><span data-stu-id="176e4-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="176e4-132">Výjimka je vyvolána v době návrhu, pokud se datové typy konfigurovaných výsledků neshodují.</span><span class="sxs-lookup"><span data-stu-id="176e4-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="176e4-133">Jsou-li první výsledná hodnota a *n*-tá hodnota výsledku hodnoty datového typu *kontejner (záznam)* nebo *seznam záznamů*, výsledek obsahuje pouze pole, která existují v obou hodnotách.</span><span class="sxs-lookup"><span data-stu-id="176e4-133">If the first result value and the *N*th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="176e4-134">Příklad</span><span class="sxs-lookup"><span data-stu-id="176e4-134">Example</span></span>

<span data-ttu-id="176e4-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` vrátí řetězec **"WINTER"** (zima), pokud je aktuální datum relace aplikace mezi říjnem a prosincem.</span><span class="sxs-lookup"><span data-stu-id="176e4-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="176e4-136">Jinak bude vrácen prázdný řetězec.</span><span class="sxs-lookup"><span data-stu-id="176e4-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="176e4-137">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="176e4-137">Additional resources</span></span>

[<span data-ttu-id="176e4-138">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="176e4-138">Logical functions</span></span>](er-functions-category-logical.md)
