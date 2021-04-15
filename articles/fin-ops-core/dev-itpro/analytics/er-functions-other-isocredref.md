---
title: Funkce elektronického výkaznictví ISOCREDREF
description: Toto téma obsahuje obecné informace o použití funkce ISOCREDREF elektronického výkaznictví.
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748310"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="b6fdb-103">Funkce elektronického výkaznictví ISOCREDREF</span><span class="sxs-lookup"><span data-stu-id="b6fdb-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6fdb-104">Funkce `ISOCREDREF` vrátí hodnotu typu *řetězec*, která představuje ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6fdb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6fdb-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="b6fdb-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b6fdb-106">Arguments</span></span>

<span data-ttu-id="b6fdb-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="b6fdb-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="b6fdb-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="b6fdb-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b6fdb-109">Return values</span></span>

<span data-ttu-id="b6fdb-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="b6fdb-110">*String*</span></span>

<span data-ttu-id="b6fdb-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b6fdb-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="b6fdb-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="b6fdb-113">Chcete-li vyloučit z abecedy symboly, které nejsou v souladu se standardem ISO, argument `invoice number digits` musí být přeložen před jeho předáním této funkci.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="b6fdb-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="b6fdb-114">Example</span></span>

<span data-ttu-id="b6fdb-115">`ISOCredRef ("VEND-200002")` vrátí **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="b6fdb-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6fdb-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b6fdb-116">Additional resources</span></span>

[<span data-ttu-id="b6fdb-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="b6fdb-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]