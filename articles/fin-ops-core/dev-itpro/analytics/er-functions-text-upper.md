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
ms.openlocfilehash: 672abf4938df7d96c0190bfd5325689b381e2764
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744328"
---
# <a name="upper-er-function"></a><span data-ttu-id="f6c9d-103">Funkce elektronického výkaznictví UPPER</span><span class="sxs-lookup"><span data-stu-id="f6c9d-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6c9d-104">Funkce `UPPER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na velká písmena.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6c9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6c9d-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="f6c9d-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f6c9d-106">Arguments</span></span>

<span data-ttu-id="f6c9d-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-107">`text`: *String*</span></span>

<span data-ttu-id="f6c9d-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f6c9d-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f6c9d-109">Return values</span></span>

<span data-ttu-id="f6c9d-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f6c9d-110">*String*</span></span>

<span data-ttu-id="f6c9d-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f6c9d-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="f6c9d-112">Example</span></span>

<span data-ttu-id="f6c9d-113">`UPPER ("Sample")` vrátí **"SAMPLE"**.</span><span class="sxs-lookup"><span data-stu-id="f6c9d-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6c9d-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f6c9d-114">Additional resources</span></span>

[<span data-ttu-id="f6c9d-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="f6c9d-115">Text functions</span></span>](er-functions-category-text.md)
