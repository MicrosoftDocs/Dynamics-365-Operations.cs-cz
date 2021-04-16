---
title: Funkce elektronického výkaznictví ORDERBY
description: Toto téma obsahuje obecné informace o použití funkce ORDERBY elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753185"
---
# <a name="orderby-er-function"></a><span data-ttu-id="39b95-103">Funkce elektronického výkaznictví ORDERBY</span><span class="sxs-lookup"><span data-stu-id="39b95-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39b95-104">Funkce `ORDERBY` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů.</span><span class="sxs-lookup"><span data-stu-id="39b95-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="39b95-105">Tyto argumenty lze definovat jako výrazy.</span><span class="sxs-lookup"><span data-stu-id="39b95-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b95-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39b95-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="39b95-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="39b95-107">Arguments</span></span>

<span data-ttu-id="39b95-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="39b95-108">`list`: *Record list*</span></span>

<span data-ttu-id="39b95-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="39b95-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="39b95-110">`expression 1`: *pole*</span><span class="sxs-lookup"><span data-stu-id="39b95-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="39b95-111">Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="39b95-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="39b95-112">Odkazované pole musí být primitivního datového typu.</span><span class="sxs-lookup"><span data-stu-id="39b95-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="39b95-113">Tento argument je povinný.</span><span class="sxs-lookup"><span data-stu-id="39b95-113">This argument is required.</span></span>

<span data-ttu-id="39b95-114">`expression N`: *pole*</span><span class="sxs-lookup"><span data-stu-id="39b95-114">`expression N`: *Field*</span></span>

<span data-ttu-id="39b95-115">Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce.</span><span class="sxs-lookup"><span data-stu-id="39b95-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="39b95-116">Odkazované pole musí být primitivního datového typu.</span><span class="sxs-lookup"><span data-stu-id="39b95-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="39b95-117">Tyto další argumenty jsou nepovinné.</span><span class="sxs-lookup"><span data-stu-id="39b95-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="39b95-118">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="39b95-118">Return values</span></span>

<span data-ttu-id="39b95-119">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="39b95-119">*Record list*</span></span>

<span data-ttu-id="39b95-120">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="39b95-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="39b95-121">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="39b95-121">Example 1</span></span>

<span data-ttu-id="39b95-122">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( ORDERBY( DS, DS. Value)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="39b95-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="39b95-123">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="39b95-123">Example 2</span></span>

<span data-ttu-id="39b95-124">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `ORDERBY (Vendors, Vendors.'name()')` vrátí seznamu dodavatelů seřazených podle názvu ve vzestupném pořadí.</span><span class="sxs-lookup"><span data-stu-id="39b95-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39b95-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="39b95-125">Additional resources</span></span>

[<span data-ttu-id="39b95-126">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="39b95-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]