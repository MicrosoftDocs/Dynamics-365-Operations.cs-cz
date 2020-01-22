---
title: Funkce el. výkaznictví NUMERALSTOTEXT
description: Toto téma obsahuje obecné informace o použití funkce NUMERALSTOTEXT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915618"
---
# <span data-ttu-id="d77a3-103"><a name="NUMERALSTOTEXT">Funkce el. výkaznictví NUMERALSTOTEXT</a></span><span class="sxs-lookup"><span data-stu-id="d77a3-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d77a3-104">Funkce `NUMERALSTOTEXT` vrací zadané číslo jako hodnotu typu *řetězec* poté, co bylo slovně vyjádřeno (tedy převedeno na textový řetězec) v zadaném jazyce.</span><span class="sxs-lookup"><span data-stu-id="d77a3-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="d77a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d77a3-105">Syntax</span></span>

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="d77a3-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d77a3-106">Arguments</span></span>

<span data-ttu-id="d77a3-107">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="d77a3-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d77a3-108">Číselná hodnota, která představuje číslo, které má být převedeno na text.</span><span class="sxs-lookup"><span data-stu-id="d77a3-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="d77a3-109">`language`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="d77a3-109">`language`: *String*</span></span>

<span data-ttu-id="d77a3-110">Hodnota typu *řetězec*, která představuje kód jazyka.</span><span class="sxs-lookup"><span data-stu-id="d77a3-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="d77a3-111">`currency`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="d77a3-111">`currency`: *String*</span></span>

<span data-ttu-id="d77a3-112">Hodnota typu *řetězec*, která představuje kód měny.</span><span class="sxs-lookup"><span data-stu-id="d77a3-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="d77a3-113">`print currency name flag`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="d77a3-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="d77a3-114">*Logická hodnota*, která označuje, zda má být k číslu převedenému na text přidán název měny.</span><span class="sxs-lookup"><span data-stu-id="d77a3-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="d77a3-115">`decimal points`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="d77a3-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="d77a3-116">*Celočíselná* hodnota označující počet desetinných míst, které má obsahovat číslo převedené na text.</span><span class="sxs-lookup"><span data-stu-id="d77a3-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="d77a3-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d77a3-117">Return values</span></span>

<span data-ttu-id="d77a3-118">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d77a3-118">*String*</span></span>

<span data-ttu-id="d77a3-119">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="d77a3-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d77a3-120">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="d77a3-120">Usage notes</span></span>

<span data-ttu-id="d77a3-121">Kód jazyka je volitelný.</span><span class="sxs-lookup"><span data-stu-id="d77a3-121">The language code is optional.</span></span> <span data-ttu-id="d77a3-122">Pokud je definován jako prázdný řetězec, použije se kód jazyka pro aktuální kontext.</span><span class="sxs-lookup"><span data-stu-id="d77a3-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="d77a3-123">Výchozí kód jazyka je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d77a3-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="d77a3-124">Kód jazyka pro spuštěný kontext je definován v prvku **Folder** nebo **File** spuštěného formátu elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="d77a3-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="d77a3-125">Zadaný kód měny je volitelný.</span><span class="sxs-lookup"><span data-stu-id="d77a3-125">The currency code is optional.</span></span> <span data-ttu-id="d77a3-126">Pokud je definován jako prázdný řetězec, použije se měna společnosti pro aktuální kontext.</span><span class="sxs-lookup"><span data-stu-id="d77a3-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="d77a3-127">Argumenty `print currency name flag` a `decimal points` jsou analyzovány pouze pro následující kódy jazyka: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** a **RU**.</span><span class="sxs-lookup"><span data-stu-id="d77a3-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="d77a3-128">Dále je argument `print currency name flag` analyzován pouze pro společnosti s kontextem země nebo oblasti, který podporuje skloňování názvů měn.</span><span class="sxs-lookup"><span data-stu-id="d77a3-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="d77a3-129">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="d77a3-129">Example 1</span></span>

<span data-ttu-id="d77a3-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` vrátí **"One Thousand Two Hundred Thirty Four and 56"**.</span><span class="sxs-lookup"><span data-stu-id="d77a3-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d77a3-131">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="d77a3-131">Example 2</span></span>

<span data-ttu-id="d77a3-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` vrátí **"sto dwadzieścia"**.</span><span class="sxs-lookup"><span data-stu-id="d77a3-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="d77a3-133">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="d77a3-133">Example 3</span></span>

<span data-ttu-id="d77a3-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` vrátí **"Сто двадцать евро 21 евроцент"**.</span><span class="sxs-lookup"><span data-stu-id="d77a3-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d77a3-135">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d77a3-135">Additional resources</span></span>

[<span data-ttu-id="d77a3-136">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="d77a3-136">Text functions</span></span>](er-functions-category-text.md)
