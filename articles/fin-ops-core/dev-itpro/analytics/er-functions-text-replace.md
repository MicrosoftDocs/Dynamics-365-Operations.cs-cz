---
title: Funkce elektronického výkaznictví REPLACE
description: Toto téma obsahuje obecné informace o použití funkce REPLACE elektronického výkaznictví.
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040979"
---
# <span data-ttu-id="5c631-103"><a name="REPLACE">Funkce elektronického výkaznictví REPLACE</a></span><span class="sxs-lookup"><span data-stu-id="5c631-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c631-104">Funkce `REPLACE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.</span><span class="sxs-lookup"><span data-stu-id="5c631-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c631-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c631-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="5c631-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5c631-106">Arguments</span></span>

<span data-ttu-id="5c631-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5c631-107">`text`: *String*</span></span>

<span data-ttu-id="5c631-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="5c631-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="5c631-109">`pattern`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5c631-109">`pattern`: *String*</span></span>

<span data-ttu-id="5c631-110">Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který je třeba nahradit.</span><span class="sxs-lookup"><span data-stu-id="5c631-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="5c631-111">Je-li argument `regular expression flag` **TRUE**, obsahuje tento argument regulární výraz, který definuje jak vyhledávací vzor, tak i nahrazující text.</span><span class="sxs-lookup"><span data-stu-id="5c631-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="5c631-112">`replacement`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5c631-112">`replacement`: *String*</span></span>

<span data-ttu-id="5c631-113">Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který se použije jako náhradní.</span><span class="sxs-lookup"><span data-stu-id="5c631-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="5c631-114">Je-li argument `regular expression flag` **TRUE**, tento argument se nepoužije.</span><span class="sxs-lookup"><span data-stu-id="5c631-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="5c631-115">`regular expression flag`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="5c631-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="5c631-116">*Logická hodnota* udává, zda se k nahrazení použje regulární výraz.</span><span class="sxs-lookup"><span data-stu-id="5c631-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="5c631-117">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5c631-117">Return values</span></span>

<span data-ttu-id="5c631-118">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="5c631-118">*String*</span></span>

<span data-ttu-id="5c631-119">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="5c631-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5c631-120">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="5c631-120">Usage notes</span></span>

<span data-ttu-id="5c631-121">Pokud má argument `regular expression flag` hodnotu **TRUE**, vrátí tato funkce zadaný řetězec poté, co byl změněn aplikováním regulárního výrazu, který je určen argumentem `pattern`.</span><span class="sxs-lookup"><span data-stu-id="5c631-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="5c631-122">Regulární výraz slouží k vyhledání znaků, které je třeba nahradit.</span><span class="sxs-lookup"><span data-stu-id="5c631-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="5c631-123">Pokud má argument `regular expression flag` hodnotu **NEPRAVDA**, chová se tato funkce stejně jako funkce [TRANSLATE](er-functions-text-translate.md).</span><span class="sxs-lookup"><span data-stu-id="5c631-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="5c631-124">Znaky zadané argumentem `replacement` se použijí k nahrazení nalezených znaků.</span><span class="sxs-lookup"><span data-stu-id="5c631-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="5c631-125">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="5c631-125">Example 1</span></span>

<span data-ttu-id="5c631-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` použije regulární výraz, který odebere všechny nenumerické symboly a vrátí **"19234564971"**.</span><span class="sxs-lookup"><span data-stu-id="5c631-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="5c631-127">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="5c631-127">Example 2</span></span>

<span data-ttu-id="5c631-128">`REPLACE ("abcdef", "cd", "GH", false)` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="5c631-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c631-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5c631-129">Additional resources</span></span>

[<span data-ttu-id="5c631-130">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="5c631-130">Text functions</span></span>](er-functions-category-text.md)
