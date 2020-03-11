---
title: Funkce elektronického výkaznictví CURCREDREF
description: Toto téma obsahuje obecné informace o použití funkce CURCREDREF elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 6e684a8e063cb3c049d13005cbcf6ebbe688af00
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041485"
---
# <span data-ttu-id="c0cdf-103"><a name="CURCREDREF">Funkce elektronického výkaznictví CURCREDREF</a></span><span class="sxs-lookup"><span data-stu-id="c0cdf-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0cdf-104">Funkce `CURCREDREF` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0cdf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0cdf-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c0cdf-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="c0cdf-106">Arguments</span></span>

<span data-ttu-id="c0cdf-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="c0cdf-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c0cdf-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c0cdf-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="c0cdf-109">Return values</span></span>

<span data-ttu-id="c0cdf-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="c0cdf-110">*String*</span></span>

<span data-ttu-id="c0cdf-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c0cdf-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="c0cdf-112">Example</span></span>

<span data-ttu-id="c0cdf-113">`CURCredRef ("VEND-200002")` vrátí **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="c0cdf-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0cdf-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c0cdf-114">Additional resources</span></span>

[<span data-ttu-id="c0cdf-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="c0cdf-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
