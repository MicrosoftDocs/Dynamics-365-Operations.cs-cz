---
title: Funkce el. výkaznictví NUMBERFORMAT
description: Toto téma obsahuje obecné informace o použití funkce NUMBERFORMAT elektronického výkaznictví.
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
ms.openlocfilehash: 41f48fb49b2d28acf69fe05fe87644a4c43e81fe
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070545"
---
# <span data-ttu-id="cefe2-103"><a name="NUMBERFORMAT">Funkce el. výkaznictví NUMBERFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="cefe2-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cefe2-104">Funkce `NUMBERFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="cefe2-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="cefe2-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="cefe2-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cefe2-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="cefe2-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="cefe2-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="cefe2-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="cefe2-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="cefe2-108">Arguments</span></span>

<span data-ttu-id="cefe2-109">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="cefe2-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="cefe2-110">Číselná hodnota, která představuje číslo, které má být formátováno.</span><span class="sxs-lookup"><span data-stu-id="cefe2-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="cefe2-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="cefe2-111">`format` : *String*</span></span>

<span data-ttu-id="cefe2-112">Hodnota typu *řetězec*, která představuje formát.</span><span class="sxs-lookup"><span data-stu-id="cefe2-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="cefe2-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="cefe2-113">`culture`: *String*</span></span>

<span data-ttu-id="cefe2-114">Hodnota typu *řetězec* představující jazykovou verzi, která má být použita pro formátování.</span><span class="sxs-lookup"><span data-stu-id="cefe2-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="cefe2-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="cefe2-115">Return values</span></span>

<span data-ttu-id="cefe2-116">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="cefe2-116">*String*</span></span>

<span data-ttu-id="cefe2-117">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="cefe2-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cefe2-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="cefe2-118">Usage notes</span></span>

<span data-ttu-id="cefe2-119">Pokud jazyková verze není definována jako argument volané funkce, kontext, ve kterém je tato funkce spuštěna, určuje jazykovou verzi, která se používá k formátování čísel.</span><span class="sxs-lookup"><span data-stu-id="cefe2-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="cefe2-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="cefe2-120">Example 1</span></span>

<span data-ttu-id="cefe2-121">Pro jazykovou verzi **EN-US** vrátí `NUMBERFORMAT (0.45, "p")` hodnotu **"45.00 %"** a `NUMBERFORMAT (10.45, "#")` vrátí hodnotu **"10"**.</span><span class="sxs-lookup"><span data-stu-id="cefe2-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cefe2-122">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="cefe2-122">Example 2</span></span>

<span data-ttu-id="cefe2-123">`NUMBERFORMAT (10/3, "F2", "de")` vrátí hodnotu **3,33**, zatímco `NUMBERFORMAT (10/3, "F2", "en-us")` vrátí **3.33**.</span><span class="sxs-lookup"><span data-stu-id="cefe2-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cefe2-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cefe2-124">Additional resources</span></span>

[<span data-ttu-id="cefe2-125">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="cefe2-125">Text functions</span></span>](er-functions-category-text.md)
