---
title: Funkce elektronického výkaznictví ISOCREDREF
description: Toto téma obsahuje obecné informace o použití funkce ISOCREDREF elektronického výkaznictví.
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
ms.openlocfilehash: d6e5d025e7de15c27b19711ea5b597d75bdf3d41
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744088"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="40373-103">Funkce elektronického výkaznictví ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="40373-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40373-104">Funkce `ISOCREDREF` vrátí hodnotu typu *řetězec*, která představuje ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="40373-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="40373-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40373-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="40373-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="40373-106">Arguments</span></span>

<span data-ttu-id="40373-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="40373-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="40373-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="40373-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="40373-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="40373-109">Return values</span></span>

<span data-ttu-id="40373-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="40373-110">*String*</span></span>

<span data-ttu-id="40373-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="40373-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="40373-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="40373-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="40373-113">Chcete-li vyloučit z abecedy symboly, které nejsou v souladu se standardem ISO, argument `invoice number digits` musí být přeložen před jeho předáním této funkci.</span><span class="sxs-lookup"><span data-stu-id="40373-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="40373-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="40373-114">Example</span></span>

<span data-ttu-id="40373-115">`ISOCredRef ("VEND-200002")` vrátí **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="40373-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40373-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="40373-116">Additional resources</span></span>

[<span data-ttu-id="40373-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="40373-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
