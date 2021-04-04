---
title: Funkce elektronického výkaznictví WHERE
description: Toto téma obsahuje obecné informace o použití funkce WHERE elektronického výkaznictví.
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
ms.openlocfilehash: ca218f87eb1f9235ab475809fbbdfecf3fe0c7fb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566035"
---
# <a name="where-er-function"></a><span data-ttu-id="5bc4e-103">Funkce elektronického výkaznictví WHERE</span><span class="sxs-lookup"><span data-stu-id="5bc4e-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5bc4e-104">Funkce `WHERE` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl filtrován podle zadané podmínky.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5bc4e-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="5bc4e-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5bc4e-106">Arguments</span></span>

<span data-ttu-id="5bc4e-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="5bc4e-107">`list`: *Record list*</span></span>

<span data-ttu-id="5bc4e-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="5bc4e-109">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="5bc4e-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="5bc4e-110">Platný podmíněný výraz, který slouží k filtrování záznamů zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="5bc4e-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5bc4e-111">Return values</span></span>

<span data-ttu-id="5bc4e-112">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="5bc4e-112">*Record list*</span></span>

<span data-ttu-id="5bc4e-113">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5bc4e-114">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="5bc4e-114">Usage notes</span></span>

<span data-ttu-id="5bc4e-115">Tato funkce se liší od funkce [FILTER](er-functions-list-filter.md), protože zadaná podmínka se použije na každý zdroj dat elektronického výkaznictví typu *seznam záznamů*, který se nachází v paměti.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="5bc4e-116">Pokud argumenty konfigurované pro tuto funkci (`list` a `condition`) umožňují překlad tohoto požadavku na přímé volání SQL, je v době návrhu vyvolána varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="5bc4e-117">Tato zpráva informuje uživatele o tom, že výkon může být zlepšen, pokud je použita funkce [FILTER](er-functions-list-filter.md) namísto funkce `WHERE`.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="5bc4e-118">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="5bc4e-118">Example 1</span></span>

<span data-ttu-id="5bc4e-119">Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `WHERE (Vendors, Vendors.VendGroup = "40")` vrátí seznam pouze dodavatelů patřících do skupiny dodavatelů č. 40.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="5bc4e-120">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="5bc4e-120">Example 2</span></span>

<span data-ttu-id="5bc4e-121">Zadáte-li zdroj dat **DS** pro typ *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `WHERE( DS, DS.Value = "B")` vrátí seznam pouze jednoho záznamu, který obsahuje text **"B"** v poli **Value**.</span><span class="sxs-lookup"><span data-stu-id="5bc4e-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bc4e-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5bc4e-122">Additional resources</span></span>

[<span data-ttu-id="5bc4e-123">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="5bc4e-123">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]