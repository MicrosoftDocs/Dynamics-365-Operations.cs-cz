---
title: Funkce el. výkaznictví DATEVALUE
description: Toto téma obsahuje obecné informace o použití funkce DATEVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682406"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="9331a-103">Funkce el. výkaznictví DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="9331a-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9331a-104">Funkce `DATEVALUE` vrátí hodnotu typu *datum*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="9331a-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="9331a-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="9331a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="9331a-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="9331a-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="9331a-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="9331a-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="9331a-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9331a-108">Arguments</span></span>

<span data-ttu-id="9331a-109">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9331a-109">`text`: *String*</span></span>

<span data-ttu-id="9331a-110">Text, který představuje hodnotu pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="9331a-110">Text that represents the value to format.</span></span>

<span data-ttu-id="9331a-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9331a-111">`format`: *String*</span></span>

<span data-ttu-id="9331a-112">Formát zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="9331a-112">The format of the given text.</span></span>

<span data-ttu-id="9331a-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9331a-113">`culture`: *String*</span></span>

<span data-ttu-id="9331a-114">Jazyková verze, která se používá pro formátování zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="9331a-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9331a-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9331a-115">Return values</span></span>

<span data-ttu-id="9331a-116">*Datum*</span><span class="sxs-lookup"><span data-stu-id="9331a-116">*Date*</span></span>

<span data-ttu-id="9331a-117">Výsledná hodnota data.</span><span class="sxs-lookup"><span data-stu-id="9331a-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9331a-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="9331a-118">Usage notes</span></span>

<span data-ttu-id="9331a-119">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="9331a-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="9331a-120">Například, pokud je funkce `DATEVALUE` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="9331a-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="9331a-121">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="9331a-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="9331a-122">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="9331a-122">Example 1</span></span>

<span data-ttu-id="9331a-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` vrátí hodnotu data **December 21, 2016** na základě zadaného vlastního formátu a výchozí jazykové verze **EN-US** aplikace.</span><span class="sxs-lookup"><span data-stu-id="9331a-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="9331a-124">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="9331a-124">Example 2</span></span>

<span data-ttu-id="9331a-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` vrátí hodnotu **21. ledna, 2016** (italsky) na základě zadaného vlastního formátu a jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="9331a-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="9331a-126">Nicméně `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` zobrazí výjimku informující uživatele, že zadaný řetězec nebyl rozpoznán jako platná hodnota data pro zadanou jazykovou verzi.</span><span class="sxs-lookup"><span data-stu-id="9331a-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9331a-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9331a-127">Additional resources</span></span>

[<span data-ttu-id="9331a-128">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="9331a-128">Date and time functions</span></span>](er-functions-category-datetime.md)
