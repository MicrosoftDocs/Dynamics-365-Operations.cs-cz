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
ms.openlocfilehash: 04c7b32e2a9578f8864570a552817ec3ce28fa43
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041146"
---
# <span data-ttu-id="51f81-103"><a name="CONCATENATE">Funkce el. výkaznictví CONCATENATE</a></span><span class="sxs-lookup"><span data-stu-id="51f81-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51f81-104">Funkce `CONCATENATE` vrátí všechny zadané textové řetězce jako hodnotu typu *řetězec* poté, co byly spojeny do jednoho řetězce.</span><span class="sxs-lookup"><span data-stu-id="51f81-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f81-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51f81-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="51f81-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="51f81-106">Arguments</span></span>

<span data-ttu-id="51f81-107">`text 1`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="51f81-107">`text 1`: *String*</span></span>

<span data-ttu-id="51f81-108">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="51f81-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="51f81-109">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="51f81-109">This argument is required.</span></span>

<span data-ttu-id="51f81-110">`text N`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="51f81-110">`text N`: *String*</span></span>

<span data-ttu-id="51f81-111">Odkaz na zdroj dat datového typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="51f81-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="51f81-112">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="51f81-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="51f81-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="51f81-113">Return values</span></span>

<span data-ttu-id="51f81-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="51f81-114">*String*</span></span>

<span data-ttu-id="51f81-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="51f81-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="51f81-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="51f81-116">Example</span></span>

<span data-ttu-id="51f81-117">`CONCATENATE ("abc", "def")` vrátí **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="51f81-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="51f81-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="51f81-118">Usage notes</span></span>

<span data-ttu-id="51f81-119">Výraz `"abc" & "def"` vrátí též **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="51f81-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51f81-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="51f81-120">Additional resources</span></span>

[<span data-ttu-id="51f81-121">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="51f81-121">Text functions</span></span>](er-functions-category-text.md)
