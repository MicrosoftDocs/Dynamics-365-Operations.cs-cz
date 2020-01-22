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
ms.openlocfilehash: 5633541b1c7e25a0cfb837c4679691506806421b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916998"
---
# <span data-ttu-id="036ea-103"><a name="CURCREDREF">Funkce elektronického výkaznictví CURCREDREF</a></span><span class="sxs-lookup"><span data-stu-id="036ea-103"><a name="CURCREDREF">CURCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="036ea-104">Funkce `CURCREDREF` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="036ea-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="036ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="036ea-105">Syntax</span></span>

```
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="036ea-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="036ea-106">Arguments</span></span>

<span data-ttu-id="036ea-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="036ea-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="036ea-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="036ea-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="036ea-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="036ea-109">Return values</span></span>

<span data-ttu-id="036ea-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="036ea-110">*String*</span></span>

<span data-ttu-id="036ea-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="036ea-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="036ea-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="036ea-112">Example</span></span>

<span data-ttu-id="036ea-113">`CURCredRef ("VEND-200002")` vrátí **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="036ea-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="036ea-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="036ea-114">Additional resources</span></span>

[<span data-ttu-id="036ea-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="036ea-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
