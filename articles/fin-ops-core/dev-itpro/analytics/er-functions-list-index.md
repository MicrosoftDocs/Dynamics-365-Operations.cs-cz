---
title: Funkce elektronického výkaznictví INDEX
description: Toto téma obsahuje obecné informace o použití funkce INDEX elektronického výkaznictví.
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
ms.openlocfilehash: 88be8f8bdc82bf3eab5c99e72046c794d8fac361
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566918"
---
# <a name="index-er-function"></a><span data-ttu-id="cb0fe-103">Funkce elektronického výkaznictví INDEX</span><span class="sxs-lookup"><span data-stu-id="cb0fe-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb0fe-104">Funkce `INDEX` vrátí hodnotu typu *kontejner (záznam)*, která je vybrána pomocí zadaného číselného indexu v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="cb0fe-105">Pokud index je mimo rozsah záznamů v zadaném seznamu, dojde k výjimce.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb0fe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb0fe-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="cb0fe-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="cb0fe-107">Arguments</span></span>

<span data-ttu-id="cb0fe-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="cb0fe-108">`list`: *Record list*</span></span>

<span data-ttu-id="cb0fe-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="cb0fe-110">`index`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="cb0fe-110">`index`: *Integer*</span></span>

<span data-ttu-id="cb0fe-111">Číselný index označující pozici požadovaného záznamu v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb0fe-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="cb0fe-112">Return values</span></span>

<span data-ttu-id="cb0fe-113">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="cb0fe-113">*Container (record)*</span></span>

<span data-ttu-id="cb0fe-114">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb0fe-115">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="cb0fe-115">Example 1</span></span>

<span data-ttu-id="cb0fe-116">Zadáte-li zdroj dat **DS** pro typ *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `DS.Value` vrátí textovou hodnotu **"B"** pro druhý záznam tohoto seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="cb0fe-117">Výraz `INDEX (SPLIT ("A|B|C", "|"), 2).Value` také vrátí textovou hodnotu **"B"**.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb0fe-118">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="cb0fe-118">Example 2</span></span>

<span data-ttu-id="cb0fe-119">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `INDEX (SPLIT ("A|B|C", "|"), 4).Value` způsobí výjimku běhu programu.</span><span class="sxs-lookup"><span data-stu-id="cb0fe-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb0fe-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cb0fe-120">Additional resources</span></span>

[<span data-ttu-id="cb0fe-121">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="cb0fe-121">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]