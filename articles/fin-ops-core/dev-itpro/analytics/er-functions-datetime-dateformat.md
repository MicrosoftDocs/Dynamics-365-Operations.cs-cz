---
title: Funkce el. výkaznictví DATEFORMAT
description: Toto téma obsahuje obecné informace o použití funkce DATEFORMAT elektronického výkaznictví.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 5a38f0016f69792e5beffa5d8224c70d6e5261c4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747028"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="32782-103">Funkce el. výkaznictví DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="32782-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32782-104">Funkce `DATEFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadanou hodnotu data jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="32782-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="32782-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="32782-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="32782-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="32782-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="32782-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="32782-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="32782-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="32782-108">Arguments</span></span>

<span data-ttu-id="32782-109">`date`: *datum*</span><span class="sxs-lookup"><span data-stu-id="32782-109">`date`: *Date*</span></span>

<span data-ttu-id="32782-110">Hodnota data, která představuje datum pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="32782-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="32782-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="32782-111">`format`: *String*</span></span>

<span data-ttu-id="32782-112">Formát výstupního řetězce.</span><span class="sxs-lookup"><span data-stu-id="32782-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="32782-113">Ve formátu řetězce se rozlišují velká a malá písmena, pokud používáte standardní formát nebo vlastní formát.</span><span class="sxs-lookup"><span data-stu-id="32782-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="32782-114">Například [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specifikátor formátu „d“ vrací datum pomocí vzoru krátkého data, zatímco standardní specifikátor formátu „D“ vrací datum pomocí vzoru dlouhého data.</span><span class="sxs-lookup"><span data-stu-id="32782-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="32782-115">Navíc [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specifikátor formátu „M“ vrací měsíc od 1 do 12, zatímco specifikátor formátu „m“ vrací minutu od 0 do 59.</span><span class="sxs-lookup"><span data-stu-id="32782-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="32782-116">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="32782-116">`culture`: *String*</span></span>

<span data-ttu-id="32782-117">Jazyková verze, která má být použita pro formátování.</span><span class="sxs-lookup"><span data-stu-id="32782-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="32782-118">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="32782-118">Return values</span></span>

<span data-ttu-id="32782-119">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="32782-119">*String*</span></span>

<span data-ttu-id="32782-120">Výsledná hodnota řetězce.</span><span class="sxs-lookup"><span data-stu-id="32782-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="32782-121">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="32782-121">Usage notes</span></span>

<span data-ttu-id="32782-122">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="32782-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="32782-123">Například, pokud je funkce `DATEFORMAT` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="32782-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="32782-124">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="32782-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="32782-125">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="32782-125">Example 1</span></span>

<span data-ttu-id="32782-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` vrátí aktuální datum aplikačního serveru, například 24. prosince 2015, jako řetězec **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="32782-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="32782-127">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="32782-127">Example 2</span></span>

<span data-ttu-id="32782-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="32782-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32782-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="32782-129">Additional resources</span></span>

[<span data-ttu-id="32782-130">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="32782-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]