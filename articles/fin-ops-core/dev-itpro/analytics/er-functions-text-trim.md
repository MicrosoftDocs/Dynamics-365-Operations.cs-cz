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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688358"
---
# <a name="trim-er-function"></a><span data-ttu-id="3760b-103">Funkce el. výkaznictví TRIM</span><span class="sxs-lookup"><span data-stu-id="3760b-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3760b-104">Funkce `TRIM` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* poté, co byly zkráceny úvodní a koncové mezery a odebrány mezery mezi slovy.</span><span class="sxs-lookup"><span data-stu-id="3760b-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3760b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3760b-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="3760b-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="3760b-106">Arguments</span></span>

<span data-ttu-id="3760b-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="3760b-107">`text`: *String*</span></span>

<span data-ttu-id="3760b-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="3760b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3760b-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="3760b-109">Return values</span></span>

<span data-ttu-id="3760b-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="3760b-110">*String*</span></span>

<span data-ttu-id="3760b-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="3760b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3760b-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="3760b-112">Example</span></span>

<span data-ttu-id="3760b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` vrátí **"Sample text"**.</span><span class="sxs-lookup"><span data-stu-id="3760b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3760b-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3760b-114">Additional resources</span></span>

[<span data-ttu-id="3760b-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="3760b-115">Text functions</span></span>](er-functions-category-text.md)
