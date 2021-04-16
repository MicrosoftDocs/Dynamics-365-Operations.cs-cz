---
title: Funkce elektronického výkaznictví REVERSE
description: Toto téma obsahuje obecné informace o použití funkce REVERSE elektronického výkaznictví.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755197"
---
# <a name="reverse-er-function"></a><span data-ttu-id="1e993-103">Funkce elektronického výkaznictví REVERSE</span><span class="sxs-lookup"><span data-stu-id="1e993-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e993-104">Funkce `REVERSE` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* v obráceném pořadí.</span><span class="sxs-lookup"><span data-stu-id="1e993-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e993-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e993-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="1e993-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="1e993-106">Arguments</span></span>

<span data-ttu-id="1e993-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="1e993-107">`list`: *Record list*</span></span>

<span data-ttu-id="1e993-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="1e993-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e993-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="1e993-109">Return values</span></span>

<span data-ttu-id="1e993-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="1e993-110">*Record list*</span></span>

<span data-ttu-id="1e993-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="1e993-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1e993-112">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="1e993-112">Example 1</span></span>

<span data-ttu-id="1e993-113">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` vrátí textovou hodnotu **"C"**.</span><span class="sxs-lookup"><span data-stu-id="1e993-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1e993-114">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="1e993-114">Example 2</span></span>

<span data-ttu-id="1e993-115">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` vrátí seznamu dodavatelů seřazených podle názvu v sestupném pořadí.</span><span class="sxs-lookup"><span data-stu-id="1e993-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e993-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1e993-116">Additional resources</span></span>

[<span data-ttu-id="1e993-117">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="1e993-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]