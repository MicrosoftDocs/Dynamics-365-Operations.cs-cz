---
title: Funkce elektronického výkaznictví REPLACE
description: Toto téma obsahuje obecné informace o použití funkce REPLACE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c9e64bd8e039b4eeca829c3c37299f002ba03592
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743728"
---
# <a name="replace-er-function"></a><span data-ttu-id="af9e4-103">Funkce elektronického výkaznictví REPLACE</span><span class="sxs-lookup"><span data-stu-id="af9e4-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af9e4-104">Funkce `REPLACE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.</span><span class="sxs-lookup"><span data-stu-id="af9e4-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af9e4-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="af9e4-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="af9e4-106">Arguments</span></span>

<span data-ttu-id="af9e4-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="af9e4-107">`text`: *String*</span></span>

<span data-ttu-id="af9e4-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="af9e4-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="af9e4-109">`pattern`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="af9e4-109">`pattern`: *String*</span></span>

<span data-ttu-id="af9e4-110">Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který je třeba nahradit.</span><span class="sxs-lookup"><span data-stu-id="af9e4-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="af9e4-111">Je-li argument `regular expression flag` **TRUE**, obsahuje tento argument regulární výraz, který definuje jak vyhledávací vzor, tak i nahrazující text.</span><span class="sxs-lookup"><span data-stu-id="af9e4-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="af9e4-112">`replacement`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="af9e4-112">`replacement`: *String*</span></span>

<span data-ttu-id="af9e4-113">Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který se použije jako náhradní.</span><span class="sxs-lookup"><span data-stu-id="af9e4-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="af9e4-114">Je-li argument `regular expression flag` **TRUE**, tento argument se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="af9e4-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="af9e4-115">`regular expression flag`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="af9e4-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="af9e4-116">*Logická hodnota* udává, zda se k nahrazení použje regulární výraz.</span><span class="sxs-lookup"><span data-stu-id="af9e4-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="af9e4-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="af9e4-117">Return values</span></span>

<span data-ttu-id="af9e4-118">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="af9e4-118">*String*</span></span>

<span data-ttu-id="af9e4-119">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="af9e4-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="af9e4-120">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="af9e4-120">Usage notes</span></span>

<span data-ttu-id="af9e4-121">Pokud má argument `regular expression flag` hodnotu **TRUE**, vrátí tato funkce zadaný řetězec poté, co byl změněn aplikováním regulárního výrazu, který je určen argumentem `pattern`.</span><span class="sxs-lookup"><span data-stu-id="af9e4-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="af9e4-122">Regulární výraz slouží k vyhledání znaků, které je třeba nahradit.</span><span class="sxs-lookup"><span data-stu-id="af9e4-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="af9e4-123">Pokud má `regular expression flag` argument hodnotu **NEPRAVDA**, vrátí tato funkce zadaný řetězec po provedení sady znaků definovaných v argumentu `pattern`, které byly nahrazeny znaky argumentu `replacement`.</span><span class="sxs-lookup"><span data-stu-id="af9e4-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="af9e4-124">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="af9e4-124">Example 1</span></span>

<span data-ttu-id="af9e4-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` použije regulární výraz, který odebere všechny nenumerické symboly a vrátí **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="af9e4-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="af9e4-126">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="af9e4-126">Example 2</span></span>

<span data-ttu-id="af9e4-127">`REPLACE ("abcdef", "cd", "GH", false)` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="af9e4-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af9e4-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="af9e4-128">Additional resources</span></span>

[<span data-ttu-id="af9e4-129">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="af9e4-129">Text functions</span></span>](er-functions-category-text.md)
