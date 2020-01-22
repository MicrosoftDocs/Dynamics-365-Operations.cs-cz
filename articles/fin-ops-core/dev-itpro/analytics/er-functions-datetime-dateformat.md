---
title: Funkce el. výkaznictví DATEFORMAT
description: Toto téma obsahuje obecné informace o použití funkce DATEFORMAT elektronického výkaznictví.
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917573"
---
# <span data-ttu-id="a3bb2-103"><a name="DATEFORMAT">Funkce el. výkaznictví DATEFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="a3bb2-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3bb2-104">Funkce `DATEFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadanou hodnotu data jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="a3bb2-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="a3bb2-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="a3bb2-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="a3bb2-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="a3bb2-106">Syntax 1</span></span>

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="a3bb2-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="a3bb2-107">Syntax 2</span></span>

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="a3bb2-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="a3bb2-108">Arguments</span></span>

<span data-ttu-id="a3bb2-109">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="a3bb2-109">`date`: *Date*</span></span>

<span data-ttu-id="a3bb2-110">Hodnota data, která představuje datum pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="a3bb2-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="a3bb2-111">`format`: *String*</span></span>

<span data-ttu-id="a3bb2-112">Formát výstupního řetězce.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-112">The format of the output string.</span></span>

<span data-ttu-id="a3bb2-113">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="a3bb2-113">`culture`: *String*</span></span>

<span data-ttu-id="a3bb2-114">Jazyková verze, která má být použita pro formátování.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3bb2-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a3bb2-115">Return values</span></span>

<span data-ttu-id="a3bb2-116">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a3bb2-116">*String*</span></span>

<span data-ttu-id="a3bb2-117">Výsledná hodnota řetězce.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a3bb2-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="a3bb2-118">Usage notes</span></span>

<span data-ttu-id="a3bb2-119">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="a3bb2-120">Například, pokud je funkce `DATEFORMAT` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="a3bb2-121">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="a3bb2-122">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="a3bb2-122">Example 1</span></span>

<span data-ttu-id="a3bb2-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="a3bb2-124">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="a3bb2-124">Example 2</span></span>

<span data-ttu-id="a3bb2-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="a3bb2-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3bb2-126">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a3bb2-126">Additional resources</span></span>

[<span data-ttu-id="a3bb2-127">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="a3bb2-127">Date and time functions</span></span>](er-functions-category-datetime.md)
