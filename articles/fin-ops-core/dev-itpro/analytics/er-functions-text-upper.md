---
title: Funkce elektronického výkaznictví UPPER
description: Toto téma obsahuje obecné informace o použití funkce UPPER elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916676"
---
# <span data-ttu-id="0d1a5-103"><a name="UPPER">Funkce elektronického výkaznictví UPPER</a></span><span class="sxs-lookup"><span data-stu-id="0d1a5-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d1a5-104">Funkce `UPPER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na velká písmena.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d1a5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d1a5-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="0d1a5-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0d1a5-106">Arguments</span></span>

<span data-ttu-id="0d1a5-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="0d1a5-107">`text`: *String*</span></span>

<span data-ttu-id="0d1a5-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d1a5-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0d1a5-109">Return values</span></span>

<span data-ttu-id="0d1a5-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="0d1a5-110">*String*</span></span>

<span data-ttu-id="0d1a5-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0d1a5-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="0d1a5-112">Example</span></span>

<span data-ttu-id="0d1a5-113">`UPPER ("Sample")` vrátí **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d1a5-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0d1a5-114">Additional resources</span></span>

[<span data-ttu-id="0d1a5-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="0d1a5-115">Text functions</span></span>](er-functions-category-text.md)
