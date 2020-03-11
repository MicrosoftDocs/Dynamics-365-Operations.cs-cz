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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042198"
---
# <span data-ttu-id="29035-103"><a name="COUNT">Funkce elektronického výkaznictví COUNT</a></span><span class="sxs-lookup"><span data-stu-id="29035-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="29035-104">Funkce `COUNT` vrátí hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="29035-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="29035-105">Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).</span><span class="sxs-lookup"><span data-stu-id="29035-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="29035-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29035-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="29035-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="29035-107">Arguments</span></span>

<span data-ttu-id="29035-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="29035-108">`list`: *Record list*</span></span>

<span data-ttu-id="29035-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="29035-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="29035-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="29035-110">Return values</span></span>

<span data-ttu-id="29035-111">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="29035-111">*Integer*</span></span>

<span data-ttu-id="29035-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="29035-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="29035-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="29035-113">Example</span></span>

<span data-ttu-id="29035-114">`COUNT (SPLIT("abcd" , 3))` vrátí hodnotu **2**, protože funkce `SPLIT` použitá v tomto příkladu vytvoří seznam obsahující dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="29035-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29035-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="29035-115">Additional resources</span></span>

[<span data-ttu-id="29035-116">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="29035-116">List functions</span></span>](er-functions-category-list.md)
