---
title: Funkce elektronického výkaznictví SPLIT
description: Toto téma obsahuje obecné informace o použití funkce SPLIT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 52a89f744cd37c543294522cc706ae7f47660e75
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070614"
---
# <span data-ttu-id="3421b-103"><a name="SPLIT">Funkce elektronického výkaznictví SPLIT</a></span><span class="sxs-lookup"><span data-stu-id="3421b-103"><a name="SPLIT">SPLIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3421b-104">Funkce `SPLIT` rozdělí zadaný vstupní řetězec do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="3421b-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3421b-105">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="3421b-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="3421b-106">Tato syntaxe rozdělí zadaný vstupní řetězec na podřetězce, přičemž každý má zadanou délku.</span><span class="sxs-lookup"><span data-stu-id="3421b-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="3421b-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="3421b-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="3421b-108">Tato syntaxe rozdělí zadaný vstupní řetězec na podřetězce na základě určeného oddělovače.</span><span class="sxs-lookup"><span data-stu-id="3421b-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="3421b-109">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3421b-109">Arguments</span></span>

<span data-ttu-id="3421b-110">`input`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3421b-110">`input`: *String*</span></span>

<span data-ttu-id="3421b-111">Text, který má být rozdělen.</span><span class="sxs-lookup"><span data-stu-id="3421b-111">The text to split.</span></span>

<span data-ttu-id="3421b-112">`length`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="3421b-112">`length`: *Integer*</span></span>

<span data-ttu-id="3421b-113">Maximální délka jednoho podřetězce.</span><span class="sxs-lookup"><span data-stu-id="3421b-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="3421b-114">`delimiter`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3421b-114">`delimiter`: *String*</span></span>

<span data-ttu-id="3421b-115">Oddělovač k oddělení dílčích řetězců.</span><span class="sxs-lookup"><span data-stu-id="3421b-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="3421b-116">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3421b-116">Return values</span></span>

<span data-ttu-id="3421b-117">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="3421b-117">*Record list*</span></span>

<span data-ttu-id="3421b-118">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="3421b-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3421b-119">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="3421b-119">Usage notes</span></span>

<span data-ttu-id="3421b-120">Struktura záznamů ve vráceném seznamu se skládá z pole **Value** typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="3421b-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="3421b-121">Každý záznam ve vráceném seznamu obsahuje vygenerované podřetězce v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="3421b-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="3421b-122">Je-li argument `delimiter` prázdný, vrátí se nový seznam, který se skládá z jednoho záznamu obsahujícího pole **Value** typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="3421b-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="3421b-123">Toto pole obsahuje vstupní text.</span><span class="sxs-lookup"><span data-stu-id="3421b-123">This field contains the input text.</span></span>

<span data-ttu-id="3421b-124">Pokud je argument `input` prázdný, vrátí se nový prázdný seznam.</span><span class="sxs-lookup"><span data-stu-id="3421b-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="3421b-125">Pokud není zadán argument `input` nebo argument `delimiter`, dojde k výjimce aplikace.</span><span class="sxs-lookup"><span data-stu-id="3421b-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="3421b-126">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="3421b-126">Example 1</span></span>

<span data-ttu-id="3421b-127">`SPLIT ("abcd", 3)` vrátí nový seznam obsahující dva záznamy s polem **Value** typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="3421b-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="3421b-128">Pole **Value** v prvním záznamu obsahuje text **"abc"** a pole **Value** v druhém záznamu obsahuje text **"d"**.</span><span class="sxs-lookup"><span data-stu-id="3421b-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3421b-129">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="3421b-129">Example 2</span></span>

<span data-ttu-id="3421b-130">`SPLIT ("XAb aBy", "aB")` vrátí nový seznam obsahující tři záznamy s poleem **Value** typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="3421b-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="3421b-131">Pole **Value** v prvním záznamu obsahuje text **"X"**, pole **Value** v druhém záznamu obsahuje text **"&nbsp;"**, a pole **Value** v třetím záznamu obsahuje text **"y"**.</span><span class="sxs-lookup"><span data-stu-id="3421b-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="3421b-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3421b-132">Additional resources</span></span>

[<span data-ttu-id="3421b-133">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="3421b-133">List functions</span></span>](er-functions-category-list.md)
