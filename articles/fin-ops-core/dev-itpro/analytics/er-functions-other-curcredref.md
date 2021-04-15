---
title: Funkce elektronického výkaznictví CURCREDREF
description: Toto téma obsahuje obecné informace o použití funkce CURCREDREF elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 65f04e23000e4d2429574db71b18b6907403855e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744336"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="d7ebe-103">Funkce elektronického výkaznictví CURCREDREF</span><span class="sxs-lookup"><span data-stu-id="d7ebe-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7ebe-104">Funkce `CURCREDREF` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="d7ebe-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ebe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ebe-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="d7ebe-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d7ebe-106">Arguments</span></span>

<span data-ttu-id="d7ebe-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="d7ebe-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="d7ebe-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="d7ebe-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7ebe-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d7ebe-109">Return values</span></span>

<span data-ttu-id="d7ebe-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="d7ebe-110">*String*</span></span>

<span data-ttu-id="d7ebe-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="d7ebe-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="d7ebe-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="d7ebe-112">Example</span></span>

<span data-ttu-id="d7ebe-113">`CURCredRef ("VEND-200002")` vrátí **"2200002"**.</span><span class="sxs-lookup"><span data-stu-id="d7ebe-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7ebe-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d7ebe-114">Additional resources</span></span>

[<span data-ttu-id="d7ebe-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="d7ebe-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]