---
title: Funkce elektronického výkaznictví INDEX
description: Toto téma obsahuje obecné informace o použití funkce INDEX elektronického výkaznictví.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087744"
---
# <a name="index-er-function"></a><span data-ttu-id="c0e83-103">Funkce elektronického výkaznictví INDEX</span><span class="sxs-lookup"><span data-stu-id="c0e83-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0e83-104">Funkce `INDEX` vrátí hodnotu typu *kontejner (záznam)*, která je vybrána pomocí zadaného číselného indexu v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="c0e83-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="c0e83-105">Pokud index je mimo rozsah záznamů v zadaném seznamu, dojde k výjimce.</span><span class="sxs-lookup"><span data-stu-id="c0e83-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e83-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0e83-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="c0e83-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="c0e83-107">Arguments</span></span>

<span data-ttu-id="c0e83-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="c0e83-108">`list`: *Record list*</span></span>

<span data-ttu-id="c0e83-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="c0e83-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="c0e83-110">`index`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="c0e83-110">`index`: *Integer*</span></span>

<span data-ttu-id="c0e83-111">Číselný index označující pozici požadovaného záznamu v zadaném seznamu.</span><span class="sxs-lookup"><span data-stu-id="c0e83-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="c0e83-112">Protože se pro tuto funkci používá číslování založené na čísle 1, zadejte hodnotu **1** pro návrat prvního záznamu ze zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="c0e83-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0e83-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="c0e83-113">Return values</span></span>

<span data-ttu-id="c0e83-114">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="c0e83-114">*Container (record)*</span></span>

<span data-ttu-id="c0e83-115">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="c0e83-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="c0e83-116">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="c0e83-116">Example 1</span></span>

<span data-ttu-id="c0e83-117">Zadáte-li zdroj dat **DS** pro typ *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `DS.Value` vrátí textovou hodnotu **"B"** pro druhý záznam tohoto seznamu záznamů.</span><span class="sxs-lookup"><span data-stu-id="c0e83-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="c0e83-118">Výraz `INDEX (SPLIT ("A|B|C", "|"), 2).Value` také vrátí textovou hodnotu **"B"**.</span><span class="sxs-lookup"><span data-stu-id="c0e83-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c0e83-119">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="c0e83-119">Example 2</span></span>

<span data-ttu-id="c0e83-120">Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `INDEX (SPLIT ("A|B|C", "|"), 4).Value` způsobí výjimku běhu programu.</span><span class="sxs-lookup"><span data-stu-id="c0e83-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0e83-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c0e83-121">Additional resources</span></span>

[<span data-ttu-id="c0e83-122">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="c0e83-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
