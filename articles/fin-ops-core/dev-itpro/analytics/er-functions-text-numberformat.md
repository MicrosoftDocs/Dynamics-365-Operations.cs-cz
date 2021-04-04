---
title: Funkce el. výkaznictví NUMBERFORMAT
description: Toto téma obsahuje obecné informace o použití funkce NUMBERFORMAT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a05a1e1c4cdb050bff30ea4710da927a537da14c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562702"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="f1c27-103">Funkce el. výkaznictví NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="f1c27-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f1c27-104">Funkce `NUMBERFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="f1c27-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="f1c27-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="f1c27-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f1c27-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="f1c27-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="f1c27-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="f1c27-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="f1c27-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f1c27-108">Arguments</span></span>

<span data-ttu-id="f1c27-109">`number`: *celé číslo* nebo *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="f1c27-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="f1c27-110">Číselná hodnota, která představuje číslo, které má být formátováno.</span><span class="sxs-lookup"><span data-stu-id="f1c27-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="f1c27-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1c27-111">`format` : *String*</span></span>

<span data-ttu-id="f1c27-112">Hodnota typu *řetězec*, která představuje formát.</span><span class="sxs-lookup"><span data-stu-id="f1c27-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="f1c27-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1c27-113">`culture`: *String*</span></span>

<span data-ttu-id="f1c27-114">Hodnota typu *řetězec* představující jazykovou verzi, která má být použita pro formátování.</span><span class="sxs-lookup"><span data-stu-id="f1c27-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="f1c27-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f1c27-115">Return values</span></span>

<span data-ttu-id="f1c27-116">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f1c27-116">*String*</span></span>

<span data-ttu-id="f1c27-117">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="f1c27-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f1c27-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="f1c27-118">Usage notes</span></span>

<span data-ttu-id="f1c27-119">Pokud jazyková verze není definována jako argument volané funkce, kontext, ve kterém je tato funkce spuštěna, určuje jazykovou verzi, která se používá k formátování čísel.</span><span class="sxs-lookup"><span data-stu-id="f1c27-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="f1c27-120">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="f1c27-120">Example 1</span></span>

<span data-ttu-id="f1c27-121">Pro jazykovou verzi **EN-US** vrátí `NUMBERFORMAT (0.45, "p")` hodnotu **"45.00 %"** a `NUMBERFORMAT (10.45, "#")` vrátí hodnotu **"10"**.</span><span class="sxs-lookup"><span data-stu-id="f1c27-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f1c27-122">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="f1c27-122">Example 2</span></span>

<span data-ttu-id="f1c27-123">`NUMBERFORMAT (10/3, "F2", "de")` vrátí hodnotu **3,33**, zatímco `NUMBERFORMAT (10/3, "F2", "en-us")` vrátí **3.33**.</span><span class="sxs-lookup"><span data-stu-id="f1c27-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1c27-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f1c27-124">Additional resources</span></span>

[<span data-ttu-id="f1c27-125">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="f1c27-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]