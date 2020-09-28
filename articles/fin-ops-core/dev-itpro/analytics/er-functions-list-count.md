---
title: Funkce elektronického výkaznictví COUNT
description: Toto téma obsahuje obecné informace o použití funkce COUNT elektronického výkaznictví.
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745338"
---
# <a name="count-er-function"></a><span data-ttu-id="907b9-103">Funkce elektronického výkaznictví COUNT</span><span class="sxs-lookup"><span data-stu-id="907b9-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="907b9-104">Funkce `COUNT` vrátí hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="907b9-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="907b9-105">Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).</span><span class="sxs-lookup"><span data-stu-id="907b9-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="907b9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="907b9-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="907b9-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="907b9-107">Arguments</span></span>

<span data-ttu-id="907b9-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="907b9-108">`list`: *Record list*</span></span>

<span data-ttu-id="907b9-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="907b9-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="907b9-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="907b9-110">Return values</span></span>

<span data-ttu-id="907b9-111">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="907b9-111">*Integer*</span></span>

<span data-ttu-id="907b9-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="907b9-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="907b9-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="907b9-113">Example</span></span>

<span data-ttu-id="907b9-114">`COUNT (SPLIT("abcd" , 3))` vrátí hodnotu **2**, protože funkce `SPLIT` použitá v tomto příkladu vytvoří seznam obsahující dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="907b9-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="907b9-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="907b9-115">Additional resources</span></span>

[<span data-ttu-id="907b9-116">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="907b9-116">List functions</span></span>](er-functions-category-list.md)
