---
title: Funkce el. výkaznictví TRANSLATE
description: Toto téma obsahuje obecné informace o použití funkce TRANSLATE elektronického výkaznictví.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916699"
---
# <span data-ttu-id="e4a66-103"><a name="TRANSLATE">Funkce el. výkaznictví TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="e4a66-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4a66-104">Funkce `TRANSLATE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.</span><span class="sxs-lookup"><span data-stu-id="e4a66-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4a66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4a66-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="e4a66-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e4a66-106">Arguments</span></span>

<span data-ttu-id="e4a66-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e4a66-107">`text`: *String*</span></span>

<span data-ttu-id="e4a66-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="e4a66-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="e4a66-109">`pattern`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e4a66-109">`pattern`: *String*</span></span>

<span data-ttu-id="e4a66-110">Text, který má být nahrazen.</span><span class="sxs-lookup"><span data-stu-id="e4a66-110">The text that must be replaced.</span></span>

<span data-ttu-id="e4a66-111">`replacement`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e4a66-111">`replacement`: *String*</span></span>

<span data-ttu-id="e4a66-112">Text, který má být použit jako náhrada.</span><span class="sxs-lookup"><span data-stu-id="e4a66-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="e4a66-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e4a66-113">Return values</span></span>

<span data-ttu-id="e4a66-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="e4a66-114">*String*</span></span>

<span data-ttu-id="e4a66-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="e4a66-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e4a66-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="e4a66-116">Example</span></span>

<span data-ttu-id="e4a66-117">`TRANSLATE ("abcdef", "cd", "GH")` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="e4a66-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4a66-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e4a66-118">Additional resources</span></span>

[<span data-ttu-id="e4a66-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="e4a66-119">Text functions</span></span>](er-functions-category-text.md)
