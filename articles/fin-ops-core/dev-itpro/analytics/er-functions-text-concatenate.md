---
title: Funkce el. výkaznictví CONCATENATE
description: Toto téma obsahuje obecné informace o použití funkce CONCATENATE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915756"
---
# <span data-ttu-id="c2787-103"><a name="CONCATENATE">Funkce el. výkaznictví CONCATENATE</a></span><span class="sxs-lookup"><span data-stu-id="c2787-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2787-104">Funkce `CONCATENATE` vrátí všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce.</span><span class="sxs-lookup"><span data-stu-id="c2787-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2787-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2787-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="c2787-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="c2787-106">Arguments</span></span>

<span data-ttu-id="c2787-107">`text 1`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="c2787-107">`text 1`: *String*</span></span>

<span data-ttu-id="c2787-108">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="c2787-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="c2787-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="c2787-109">This argument is required.</span></span>

<span data-ttu-id="c2787-110">`text N`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="c2787-110">`text N`: *String*</span></span>

<span data-ttu-id="c2787-111">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="c2787-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="c2787-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="c2787-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2787-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="c2787-113">Return values</span></span>

<span data-ttu-id="c2787-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="c2787-114">*String*</span></span>

<span data-ttu-id="c2787-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="c2787-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c2787-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="c2787-116">Example</span></span>

<span data-ttu-id="c2787-117">`CONCATENATE ("abc", "def")` vrátí **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="c2787-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c2787-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="c2787-118">Usage notes</span></span>

<span data-ttu-id="c2787-119">Výraz `"abc" & "def"` vrátí též **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="c2787-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2787-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c2787-120">Additional resources</span></span>

[<span data-ttu-id="c2787-121">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="c2787-121">Text functions</span></span>](er-functions-category-text.md)
