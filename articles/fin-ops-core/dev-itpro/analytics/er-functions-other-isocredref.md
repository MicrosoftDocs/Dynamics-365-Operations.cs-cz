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
ms.openlocfilehash: dd692720872314d533274f392f84e5ac7d36c7c1
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041370"
---
# <span data-ttu-id="baca5-103"><a name="ISOCREDREF">Funkce elektronického výkaznictví ISOCREDREF</a></span><span class="sxs-lookup"><span data-stu-id="baca5-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baca5-104">Funkce `ISOCREDREF` vrátí hodnotu typu *řetězec*, která představuje ISO údaj věřitele na základě číslic a abecedních symbolů zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="baca5-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="baca5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="baca5-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="baca5-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="baca5-106">Arguments</span></span>

<span data-ttu-id="baca5-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="baca5-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="baca5-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="baca5-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="baca5-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="baca5-109">Return values</span></span>

<span data-ttu-id="baca5-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="baca5-110">*String*</span></span>

<span data-ttu-id="baca5-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="baca5-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="baca5-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="baca5-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="baca5-113">Chcete-li vyloučit z abecedy symboly, které nejsou v souladu se standardem ISO, argument `invoice number digits` musí být přeložen před jeho předáním této funkci.</span><span class="sxs-lookup"><span data-stu-id="baca5-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="baca5-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="baca5-114">Example</span></span>

<span data-ttu-id="baca5-115">`ISOCredRef ("VEND-200002")` vrátí **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="baca5-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="baca5-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="baca5-116">Additional resources</span></span>

[<span data-ttu-id="baca5-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="baca5-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
