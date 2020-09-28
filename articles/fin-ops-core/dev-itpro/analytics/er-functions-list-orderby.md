---
title: Funkce elektronického výkaznictví ORDERBY
description: Toto téma obsahuje obecné informace o použití funkce ORDERBY elektronického výkaznictví.
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
ms.openlocfilehash: 6ff280d66fd2c418984f2d7fd31a32609932e89c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745002"
---
# <a name="orderby-er-function"></a><span data-ttu-id="15891-103">Funkce elektronického výkaznictví ORDERBY</span><span class="sxs-lookup"><span data-stu-id="15891-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15891-104">Funkce `ORDERBY` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="15891-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="15891-105">Tyto argumenty lze definovat jako výrazy.</span><span class="sxs-lookup"><span data-stu-id="15891-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="15891-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15891-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="15891-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="15891-107">Arguments</span></span>

<span data-ttu-id="15891-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="15891-108">`list`: *Record list*</span></span>

<span data-ttu-id="15891-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="15891-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="15891-110">`expression 1`: *pole*</span><span class="sxs-lookup"><span data-stu-id="15891-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="15891-111">Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="15891-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="15891-112">Odkazované pole musí být primitivního datového typu.</span><span class="sxs-lookup"><span data-stu-id="15891-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="15891-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="15891-113">This argument is required.</span></span>

<span data-ttu-id="15891-114">`expression N`: *pole*</span><span class="sxs-lookup"><span data-stu-id="15891-114">`expression N`: *Field*</span></span>

<span data-ttu-id="15891-115">Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="15891-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="15891-116">Odkazované pole musí být primitivního datového typu.</span><span class="sxs-lookup"><span data-stu-id="15891-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="15891-117">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="15891-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="15891-118">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="15891-118">Return values</span></span>

<span data-ttu-id="15891-119">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="15891-119">*Record list*</span></span>

<span data-ttu-id="15891-120">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="15891-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="15891-121">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="15891-121">Example 1</span></span>

<span data-ttu-id="15891-122">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( ORDERBY( DS, DS. Value)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="15891-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="15891-123">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="15891-123">Example 2</span></span>

<span data-ttu-id="15891-124">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `ORDERBY (Vendors, Vendors.'name()')` vrátí seznamu dodavatelů seřazených podle názvu ve vzestupném pořadí.</span><span class="sxs-lookup"><span data-stu-id="15891-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15891-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="15891-125">Additional resources</span></span>

[<span data-ttu-id="15891-126">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="15891-126">List functions</span></span>](er-functions-category-list.md)
