---
title: Funkce el. výkaznictví TRIM
description: Toto téma obsahuje obecné informace o použití funkce TRIM elektronického výkaznictví.
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
ms.openlocfilehash: a1f7999ccbcd167280cca1abc48377c36d2bc15f
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744208"
---
# <a name="trim-er-function"></a><span data-ttu-id="1815f-103">Funkce el. výkaznictví TRIM</span><span class="sxs-lookup"><span data-stu-id="1815f-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1815f-104">Funkce `TRIM` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* poté, co byly zkráceny úvodní a koncové mezery a odebrány mezery mezi slovy.</span><span class="sxs-lookup"><span data-stu-id="1815f-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1815f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1815f-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="1815f-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="1815f-106">Arguments</span></span>

<span data-ttu-id="1815f-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="1815f-107">`text`: *String*</span></span>

<span data-ttu-id="1815f-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="1815f-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1815f-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="1815f-109">Return values</span></span>

<span data-ttu-id="1815f-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="1815f-110">*String*</span></span>

<span data-ttu-id="1815f-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="1815f-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1815f-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="1815f-112">Example</span></span>

<span data-ttu-id="1815f-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` vrátí **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="1815f-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1815f-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1815f-114">Additional resources</span></span>

[<span data-ttu-id="1815f-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="1815f-115">Text functions</span></span>](er-functions-category-text.md)
