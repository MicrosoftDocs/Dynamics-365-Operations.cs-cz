---
title: Funkce el. výkaznictví DATETIMEVALUE
description: Toto téma obsahuje obecné informace o použití funkce DATETIMEVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 65eb16c5846b5d194361940667da14b594d7a63c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744880"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="e8a8b-103">Funkce el. výkaznictví DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="e8a8b-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8a8b-104">Funkce `DATETIMEVALUE` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="e8a8b-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="e8a8b-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e8a8b-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e8a8b-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="e8a8b-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e8a8b-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="e8a8b-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e8a8b-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e8a8b-108">Arguments</span></span>

<span data-ttu-id="e8a8b-109">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e8a8b-109">`text`: *String*</span></span>

<span data-ttu-id="e8a8b-110">Text, který představuje hodnotu pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-110">Text that represents the value to format.</span></span>

<span data-ttu-id="e8a8b-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e8a8b-111">`format`: *String*</span></span>

<span data-ttu-id="e8a8b-112">Formát zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-112">The format of the given text.</span></span>

<span data-ttu-id="e8a8b-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e8a8b-113">`culture`: *String*</span></span>

<span data-ttu-id="e8a8b-114">Jazyková verze, která se používá pro formátování zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8a8b-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e8a8b-115">Return values</span></span>

<span data-ttu-id="e8a8b-116">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="e8a8b-116">*DateTime*</span></span>

<span data-ttu-id="e8a8b-117">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e8a8b-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="e8a8b-118">Usage notes</span></span>

<span data-ttu-id="e8a8b-119">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e8a8b-120">Například, pokud je funkce `DATETIMEVALUE` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e8a8b-121">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="e8a8b-122">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="e8a8b-122">Example 1</span></span>

<span data-ttu-id="e8a8b-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` vrátí **2:55:00 AM on December 21, 2016** na základě zadaného vlastního formátu a výchozí jazykové verze **EN-US** aplikace.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="e8a8b-124">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="e8a8b-124">Example 2</span></span>

<span data-ttu-id="e8a8b-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` vrátí **2:55:00, 21. ledna 2016** (italsky) na základě zadaného vlastního formátu a jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="e8a8b-126">Nicméně `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` zobrazí výjimku informující uživatele, že zadaný řetězec nebyl rozpoznán jako platná hodnota data/času pro zadanou jazykovou verzi.</span><span class="sxs-lookup"><span data-stu-id="e8a8b-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8a8b-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e8a8b-127">Additional resources</span></span>

[<span data-ttu-id="e8a8b-128">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="e8a8b-128">Date and time functions</span></span>](er-functions-category-datetime.md)
