---
title: Funkce el. výkaznictví DATETIMEFORMAT
description: Toto téma obsahuje obecné informace o použití funkce DATETIMEFORMAT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
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
ms.openlocfilehash: 90bd2900434b1be509f72ec82375e52ea32bc424
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/04/2021
ms.locfileid: "4825366"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="86f0a-103">Funkce el. výkaznictví DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="86f0a-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86f0a-104">Funkce `DATETIMEFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadanou hodnotu data/času jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="86f0a-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="86f0a-105">Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="86f0a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="86f0a-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="86f0a-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="86f0a-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="86f0a-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="86f0a-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="86f0a-108">Arguments</span></span>

<span data-ttu-id="86f0a-109">`datetime`: *datum a čas*</span><span class="sxs-lookup"><span data-stu-id="86f0a-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="86f0a-110">Hodnota data/času, která představuje datum a čas pro zformátování.</span><span class="sxs-lookup"><span data-stu-id="86f0a-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="86f0a-111">`format`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="86f0a-111">`format`: *String*</span></span>

<span data-ttu-id="86f0a-112">Formát výstupního řetězce.</span><span class="sxs-lookup"><span data-stu-id="86f0a-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="86f0a-113">Ve formátu řetězce se rozlišují velká a malá písmena, pokud používáte standardní formát nebo vlastní formát.</span><span class="sxs-lookup"><span data-stu-id="86f0a-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="86f0a-114">Například [standardní](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) specifikátor formátu „d“ vrací datum pomocí vzoru krátkého data, zatímco standardní specifikátor formátu „D“ vrací datum pomocí vzoru dlouhého data.</span><span class="sxs-lookup"><span data-stu-id="86f0a-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="86f0a-115">Navíc [vlastní](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) specifikátor formátu „M“ vrací měsíc od 1 do 12, zatímco specifikátor formátu „m“ vrací minutu od 0 do 59.</span><span class="sxs-lookup"><span data-stu-id="86f0a-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="86f0a-116">`culture`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="86f0a-116">`culture`: *String*</span></span>

<span data-ttu-id="86f0a-117">Jazyková verze, která má být použita pro formátování.</span><span class="sxs-lookup"><span data-stu-id="86f0a-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="86f0a-118">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="86f0a-118">Return values</span></span>

<span data-ttu-id="86f0a-119">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="86f0a-119">*String*</span></span>

<span data-ttu-id="86f0a-120">Výsledná hodnota řetězce.</span><span class="sxs-lookup"><span data-stu-id="86f0a-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="86f0a-121">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="86f0a-121">Usage notes</span></span>

<span data-ttu-id="86f0a-122">Pokud není jazyková verze definována jako argument volané funkce, hodnota `culture` je definovaná kontextem volání.</span><span class="sxs-lookup"><span data-stu-id="86f0a-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="86f0a-123">Například, pokud je funkce `DATETIMEFORMAT` volána pomocí syntaxe 1 ve formátu elektronického výkaznictví (ER) pro prvek **FILE**, který je konfigurován pro použití německé jazykové verze, převod se provede pomocí německé jazykové verze.</span><span class="sxs-lookup"><span data-stu-id="86f0a-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="86f0a-124">Výchozí hodnota `culture` je **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="86f0a-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="86f0a-125">Když funkce `DATETIMEFORMAT` převádí zadanou hodnotu data/času, bere v potaz nastavení časového pásma uživatele aplikace, který používá formát elektronického výkaznictví, v jehož kontextu je funkce volána.</span><span class="sxs-lookup"><span data-stu-id="86f0a-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="86f0a-126">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="86f0a-126">Example 1</span></span>

<span data-ttu-id="86f0a-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` vrátí aktuální datum/čas aplikačního serveru, například 24. prosince 2015 jako **"24-12-2015"** na základě zadaného vlastního formátu.</span><span class="sxs-lookup"><span data-stu-id="86f0a-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="86f0a-128">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="86f0a-128">Example 2</span></span>

<span data-ttu-id="86f0a-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` vrátí aktuální datum a čas relace aplikace, 24. prosince 2015, jako **"24.12.2015"** na základě vybrané německé jazykové verze a zadaného formátu.</span><span class="sxs-lookup"><span data-stu-id="86f0a-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="86f0a-130">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="86f0a-130">Example 3</span></span>

<span data-ttu-id="86f0a-131">Funkce `DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` vrátí řetězcovou hodnotu **2019-11-12T 08:00:00.0000000-08:00**, když je volána během procesu, který byl iniciován uživatelem aplikace, který má hodnotu časového pásma **(GMT-08:00) Tichomoří (USA a Kanada)** v sekci **Předvolby jazyka a země/oblasti**.</span><span class="sxs-lookup"><span data-stu-id="86f0a-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86f0a-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="86f0a-132">Additional resources</span></span>

[<span data-ttu-id="86f0a-133">Funkce data a času</span><span class="sxs-lookup"><span data-stu-id="86f0a-133">Date and time functions</span></span>](er-functions-category-datetime.md)
