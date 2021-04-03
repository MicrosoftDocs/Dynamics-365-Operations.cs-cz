---
title: Funkce elektronického výkaznictví COUNT
description: Toto téma obsahuje obecné informace o použití funkce COUNT elektronického výkaznictví.
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
ms.openlocfilehash: e36347d928148e85bc9295d529cbf2801946433a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567885"
---
# <a name="count-er-function"></a><span data-ttu-id="51052-103">Funkce elektronického výkaznictví COUNT</span><span class="sxs-lookup"><span data-stu-id="51052-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51052-104">Funkce `COUNT` vrátí hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="51052-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="51052-105">Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).</span><span class="sxs-lookup"><span data-stu-id="51052-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="51052-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51052-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="51052-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="51052-107">Arguments</span></span>

<span data-ttu-id="51052-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="51052-108">`list`: *Record list*</span></span>

<span data-ttu-id="51052-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="51052-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="51052-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="51052-110">Return values</span></span>

<span data-ttu-id="51052-111">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="51052-111">*Integer*</span></span>

<span data-ttu-id="51052-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="51052-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="51052-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="51052-113">Example</span></span>

<span data-ttu-id="51052-114">`COUNT (SPLIT("abcd" , 3))` vrátí hodnotu **2**, protože funkce `SPLIT` použitá v tomto příkladu vytvoří seznam obsahující dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="51052-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51052-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="51052-115">Additional resources</span></span>

[<span data-ttu-id="51052-116">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="51052-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]