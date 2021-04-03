---
title: Funkce el. výkaznictví CONCATENATE
description: Toto téma obsahuje obecné informace o použití funkce CONCATENATE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 6e4800ce44d9da07818acec55c50224a9a000fe6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569598"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="9c9e2-103">Funkce el. výkaznictví CONCATENATE</span><span class="sxs-lookup"><span data-stu-id="9c9e2-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c9e2-104">Funkce `CONCATENATE` vrátí všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c9e2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c9e2-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="9c9e2-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9c9e2-106">Arguments</span></span>

<span data-ttu-id="9c9e2-107">`text 1`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9c9e2-107">`text 1`: *String*</span></span>

<span data-ttu-id="9c9e2-108">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9c9e2-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-109">This argument is required.</span></span>

<span data-ttu-id="9c9e2-110">`text N`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9c9e2-110">`text N`: *String*</span></span>

<span data-ttu-id="9c9e2-111">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="9c9e2-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c9e2-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9c9e2-113">Return values</span></span>

<span data-ttu-id="9c9e2-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="9c9e2-114">*String*</span></span>

<span data-ttu-id="9c9e2-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9c9e2-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="9c9e2-116">Example</span></span>

<span data-ttu-id="9c9e2-117">`CONCATENATE ("abc", "def")` vrátí **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9c9e2-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="9c9e2-118">Usage notes</span></span>

<span data-ttu-id="9c9e2-119">Výraz `"abc" & "def"` vrátí též **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="9c9e2-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c9e2-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9c9e2-120">Additional resources</span></span>

[<span data-ttu-id="9c9e2-121">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="9c9e2-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]