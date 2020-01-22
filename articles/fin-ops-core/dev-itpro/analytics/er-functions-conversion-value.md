---
title: Funkce VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917619"
---
# <span data-ttu-id="e8188-103"><a name="VALUE">Funkce VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="e8188-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8188-104">Funkce `VALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="e8188-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8188-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8188-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="e8188-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e8188-106">Arguments</span></span>

<span data-ttu-id="e8188-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="e8188-107">`text`: *String*</span></span>

<span data-ttu-id="e8188-108">Hodnota řetězce, která musí být převedena na číselnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e8188-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8188-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e8188-109">Return values</span></span>

<span data-ttu-id="e8188-110">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="e8188-110">*Real*</span></span>

<span data-ttu-id="e8188-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="e8188-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e8188-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="e8188-112">Usage notes</span></span>

<span data-ttu-id="e8188-113">Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko.</span><span class="sxs-lookup"><span data-stu-id="e8188-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="e8188-114">Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, je vyvolána výjimka v době běhu.</span><span class="sxs-lookup"><span data-stu-id="e8188-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="e8188-115">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="e8188-115">Example 1</span></span>

<span data-ttu-id="e8188-116">`VALUE ("1 234,56")` zahodí výjimku.</span><span class="sxs-lookup"><span data-stu-id="e8188-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="e8188-117">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="e8188-117">Example 2</span></span>

<span data-ttu-id="e8188-118">`VALUE ("1234,56")` vrací **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="e8188-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8188-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e8188-119">Additional resources</span></span>

[<span data-ttu-id="e8188-120">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="e8188-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
