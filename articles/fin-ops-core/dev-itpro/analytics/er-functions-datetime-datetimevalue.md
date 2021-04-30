---
title: Funkce el. výkaznictví DATETIMEVALUE
description: Toto téma obsahuje obecné informace o použití funkce DATETIMEVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891274"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="fbada-103">Funkce el. výkaznictví DATETIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="fbada-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fbada-104">Funkce `DATETIMEVALUE` vrátí hodnotu typu *datum a čas*, která je převedena ze zadané textové hodnoty v určeném formátu a ve volitelně zadané [jazykové verzi](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="fbada-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="fbada-105">Informace o podporovaných formátech: [standardní](/dotnet/standard/base-types/standard-date-and-time-format-strings) a [vlastní](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="fbada-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="fbada-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="fbada-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="fbada-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="fbada-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="fbada-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="fbada-108">Arguments</span></span>

<span data-ttu-id="fbada-109">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fbada-109">`text`: *String*</span></span>

<span data-ttu-id="fbada-110">Text, který představuje hodnotu pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="fbada-110">Text that represents the value to format.</span></span>

<span data-ttu-id="fbada-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fbada-111">`format`: *String*</span></span>

<span data-ttu-id="fbada-112">Formát zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="fbada-112">The format of the given text.</span></span>

<span data-ttu-id="fbada-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fbada-113">`culture`: *String*</span></span>

<span data-ttu-id="fbada-114">Jazyková verze, která se používá pro formátování zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="fbada-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="fbada-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="fbada-115">Return values</span></span>

<span data-ttu-id="fbada-116">*Datum a čas*</span><span class="sxs-lookup"><span data-stu-id="fbada-116">*DateTime*</span></span>

<span data-ttu-id="fbada-117">Výsledná hodnota data a času.</span><span class="sxs-lookup"><span data-stu-id="fbada-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fbada-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="fbada-118">Usage notes</span></span>

<span data-ttu-id="fbada-119">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="fbada-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="fbada-120">Například, pokud je funkce `DATETIMEVALUE` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="fbada-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="fbada-121">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="fbada-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="fbada-122">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="fbada-122">Example 1</span></span>

<span data-ttu-id="fbada-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` vrátí **2:55:00 AM on December 21, 2016** na základě zadaného vlastního formátu a výchozí jazykové verze **EN-US** aplikace.</span><span class="sxs-lookup"><span data-stu-id="fbada-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="fbada-124">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="fbada-124">Example 2</span></span>

<span data-ttu-id="fbada-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` vrátí **2:55:00, 21. ledna 2016** (italsky) na základě zadaného vlastního formátu a jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="fbada-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="fbada-126">Nicméně `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` zobrazí výjimku informující uživatele, že zadaný řetězec nebyl rozpoznán jako platná hodnota data/času pro zadanou jazykovou verzi.</span><span class="sxs-lookup"><span data-stu-id="fbada-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fbada-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fbada-127">Additional resources</span></span>

[<span data-ttu-id="fbada-128">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="fbada-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]