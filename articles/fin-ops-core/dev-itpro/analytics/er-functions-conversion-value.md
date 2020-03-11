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
ms.openlocfilehash: c90772ca1e93500ac45cc52ba92d4169c4d29bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042612"
---
# <span data-ttu-id="01d14-103"><a name="VALUE">Funkce VALUE ER</a></span><span class="sxs-lookup"><span data-stu-id="01d14-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01d14-104">Funkce `VALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="01d14-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="01d14-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01d14-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="01d14-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="01d14-106">Arguments</span></span>

<span data-ttu-id="01d14-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="01d14-107">`text`: *String*</span></span>

<span data-ttu-id="01d14-108">Hodnota řetězce, která musí být převedena na číselnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01d14-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="01d14-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="01d14-109">Return values</span></span>

<span data-ttu-id="01d14-110">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="01d14-110">*Real*</span></span>

<span data-ttu-id="01d14-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="01d14-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="01d14-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="01d14-112">Usage notes</span></span>

<span data-ttu-id="01d14-113">Čárky a tečky (.) jsou považovány za oddělovače desetinných míst a úvodní spojovník (-) se používá jako záporné znaménko.</span><span class="sxs-lookup"><span data-stu-id="01d14-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="01d14-114">Pokud jsou v zadaném řetězci obsaženy jiné než číselné znaky, je vyvolána výjimka v době běhu.</span><span class="sxs-lookup"><span data-stu-id="01d14-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="01d14-115">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="01d14-115">Example 1</span></span>

<span data-ttu-id="01d14-116">`VALUE ("1 234,56")` zahodí výjimku.</span><span class="sxs-lookup"><span data-stu-id="01d14-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="01d14-117">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="01d14-117">Example 2</span></span>

<span data-ttu-id="01d14-118">`VALUE ("1234,56")` vrací **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="01d14-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01d14-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="01d14-119">Additional resources</span></span>

[<span data-ttu-id="01d14-120">Funkce převodu typu</span><span class="sxs-lookup"><span data-stu-id="01d14-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
