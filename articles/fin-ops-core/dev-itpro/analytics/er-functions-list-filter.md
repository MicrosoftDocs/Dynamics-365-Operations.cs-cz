---
title: Funkce elektronického výkaznictví FILTER
description: Toto téma obsahuje obecné informace o použití funkce FILTER elektronického výkaznictví.
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
ms.openlocfilehash: 2783fbfa0ba45c8d3772cf9ca16d110549d227b4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917366"
---
# <span data-ttu-id="2f816-103"><a name="FILTER">Funkce elektronického výkaznictví FILTER</a></span><span class="sxs-lookup"><span data-stu-id="2f816-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f816-104">Funkce `FILTER` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* po změně dotazu, který jej filtruje podle zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="2f816-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f816-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f816-105">Syntax</span></span>

```
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="2f816-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2f816-106">Arguments</span></span>

<span data-ttu-id="2f816-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="2f816-107">`list`: *Record list*</span></span>

<span data-ttu-id="2f816-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="2f816-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="2f816-109">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="2f816-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="2f816-110">Platný podmíněný výraz, který slouží k filtrování záznamů zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="2f816-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="2f816-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2f816-111">Return values</span></span>

<span data-ttu-id="2f816-112">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="2f816-112">*Record list*</span></span>

<span data-ttu-id="2f816-113">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="2f816-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2f816-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="2f816-114">Usage notes</span></span>

<span data-ttu-id="2f816-115">Tato funkce se liší od funkce [WHERE](er-functions-list-where.md), protože zadaná podmínka je použita u jakéhokoli zdroje dat elektronického výkaznictví typu *Záznamy tabulky* na úrovni databáze.</span><span class="sxs-lookup"><span data-stu-id="2f816-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="2f816-116">Seznam a podmínku lze definovat pomocí tabulek a relací.</span><span class="sxs-lookup"><span data-stu-id="2f816-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="2f816-117">Pokud jeden či více argumentů konfigurovaných pro tuto funkci (`list` a `condition`) neumožňuje překlad tohoto požadavku na přímé volání SQL, dojde v době návrhu k výjimce.</span><span class="sxs-lookup"><span data-stu-id="2f816-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="2f816-118">Tato výjimka informuje uživatele, že k dotazování databáze nelze použít `list` nebo `condition`.</span><span class="sxs-lookup"><span data-stu-id="2f816-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="2f816-119">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="2f816-119">Example 1</span></span>

<span data-ttu-id="2f816-120">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `FILTER (Vendors, Vendors.VendGroup = "40")` vrátí seznam pouze dodavatelů patřících do skupiny dodavatelů č. 40.</span><span class="sxs-lookup"><span data-stu-id="2f816-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="2f816-121">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="2f816-121">Example 2</span></span>

<span data-ttu-id="2f816-122">Pokud je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který se vztahuje k tabulce VendTable a pokud je parametr **parmVendorBankGroup** konfigurován jako zdroj dat elektronického výkaznictví, který vrací hodnotu datového typu *řetězec*, výraz `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` vrátí seznam pouze těch dodavatelských účtů, které patří ke konkrétní bankovní skupině.</span><span class="sxs-lookup"><span data-stu-id="2f816-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="2f816-123">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="2f816-123">Example 3</span></span>

<span data-ttu-id="2f816-124">Zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="2f816-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="2f816-125">Potom zadáte jiný výraz `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="2f816-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="2f816-126">Při pokusu o uložení tohoto výrazu v návrháři receptur elektronického výkaznictví je vyvolána následující výjimka: „Chyba ověření: na výraz seznamu funkce FILTER se nelze dotazovat.“</span><span class="sxs-lookup"><span data-stu-id="2f816-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f816-127">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2f816-127">Additional resources</span></span>

[<span data-ttu-id="2f816-128">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="2f816-128">List functions</span></span>](er-functions-category-list.md)