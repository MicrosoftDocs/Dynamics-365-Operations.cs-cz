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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040909"
---
# <span data-ttu-id="37cf7-103"><a name="TRANSLATE">Funkce el. výkaznictví TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="37cf7-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37cf7-104">Funkce `TRANSLATE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.</span><span class="sxs-lookup"><span data-stu-id="37cf7-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cf7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37cf7-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="37cf7-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="37cf7-106">Arguments</span></span>

<span data-ttu-id="37cf7-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="37cf7-107">`text`: *String*</span></span>

<span data-ttu-id="37cf7-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="37cf7-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="37cf7-109">`pattern`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="37cf7-109">`pattern`: *String*</span></span>

<span data-ttu-id="37cf7-110">Text, který má být nahrazen.</span><span class="sxs-lookup"><span data-stu-id="37cf7-110">The text that must be replaced.</span></span>

<span data-ttu-id="37cf7-111">`replacement`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="37cf7-111">`replacement`: *String*</span></span>

<span data-ttu-id="37cf7-112">Text, který má být použit jako náhrada.</span><span class="sxs-lookup"><span data-stu-id="37cf7-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="37cf7-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="37cf7-113">Return values</span></span>

<span data-ttu-id="37cf7-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="37cf7-114">*String*</span></span>

<span data-ttu-id="37cf7-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="37cf7-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="37cf7-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="37cf7-116">Example</span></span>

<span data-ttu-id="37cf7-117">`TRANSLATE ("abcdef", "cd", "GH")` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.</span><span class="sxs-lookup"><span data-stu-id="37cf7-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37cf7-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="37cf7-118">Additional resources</span></span>

[<span data-ttu-id="37cf7-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="37cf7-119">Text functions</span></span>](er-functions-category-text.md)
