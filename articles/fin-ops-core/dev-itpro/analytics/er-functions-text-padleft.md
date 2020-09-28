---
title: Funkce el. výkaznictví PADLEFT
description: Toto téma obsahuje obecné informace o použití funkce PADLEFT elektronického výkaznictví.
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744352"
---
# <a name="padleft-er-function"></a><span data-ttu-id="07de0-103">Funkce el. výkaznictví PADLEFT</span><span class="sxs-lookup"><span data-stu-id="07de0-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07de0-104">Funkce `PADLEFT` vrátí hodnotu typu *řetězec* zadané délky, kde je začátek zadaného řetězce odsazen určenými znaky.</span><span class="sxs-lookup"><span data-stu-id="07de0-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="07de0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07de0-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="07de0-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="07de0-106">Arguments</span></span>

<span data-ttu-id="07de0-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="07de0-107">`text`: *String*</span></span>

<span data-ttu-id="07de0-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="07de0-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="07de0-109">`length`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="07de0-109">`length`: *Integer*</span></span>

<span data-ttu-id="07de0-110">*Celočíselná* hodnota, která představuje konečný počet znaků odsazeného řetězce.</span><span class="sxs-lookup"><span data-stu-id="07de0-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="07de0-111">`padding chars`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="07de0-111">`padding chars`: *String*</span></span>

<span data-ttu-id="07de0-112">Znaky, které mají být použity pro odsazení.</span><span class="sxs-lookup"><span data-stu-id="07de0-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="07de0-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="07de0-113">Return values</span></span>

<span data-ttu-id="07de0-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="07de0-114">*String*</span></span>

<span data-ttu-id="07de0-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="07de0-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="07de0-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="07de0-116">Example</span></span>

<span data-ttu-id="07de0-117">`PADLEFT ("1234", 10, "`&nbsp;`")` vrátí textový řetězec **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="07de0-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07de0-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="07de0-118">Additional resources</span></span>

[<span data-ttu-id="07de0-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="07de0-119">Text functions</span></span>](er-functions-category-text.md)
