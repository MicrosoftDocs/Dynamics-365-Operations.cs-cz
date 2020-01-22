---
title: Funkce elektronického výkaznictví REVERSE
description: Toto téma obsahuje obecné informace o použití funkce REVERSE elektronického výkaznictví.
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
ms.openlocfilehash: 3343ad788cef29a79f9b110bf29809cd5f0e5c63
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917228"
---
# <span data-ttu-id="79839-103"><a name="REVERSE">Funkce elektronického výkaznictví REVERSE</a></span><span class="sxs-lookup"><span data-stu-id="79839-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79839-104">Funkce `REVERSE` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* v obráceném pořadí.</span><span class="sxs-lookup"><span data-stu-id="79839-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="79839-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79839-105">Syntax</span></span>

```
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="79839-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="79839-106">Arguments</span></span>

<span data-ttu-id="79839-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="79839-107">`list`: *Record list*</span></span>

<span data-ttu-id="79839-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="79839-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="79839-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="79839-109">Return values</span></span>

<span data-ttu-id="79839-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="79839-110">*Record list*</span></span>

<span data-ttu-id="79839-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="79839-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="79839-112">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="79839-112">Example 1</span></span>

<span data-ttu-id="79839-113">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` vrátí textovou hodnotu **"C"**.</span><span class="sxs-lookup"><span data-stu-id="79839-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="79839-114">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="79839-114">Example 2</span></span>

<span data-ttu-id="79839-115">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` vrátí seznamu dodavatelů seřazených podle názvu v sestupném pořadí.</span><span class="sxs-lookup"><span data-stu-id="79839-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="79839-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="79839-116">Additional resources</span></span>

[<span data-ttu-id="79839-117">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="79839-117">List functions</span></span>](er-functions-category-list.md)
