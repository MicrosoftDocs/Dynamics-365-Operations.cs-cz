---
title: Funkce el. výkaznictví CH_BANK_MOD_10
description: Toto téma obsahuje obecné informace o použití funkce CH_BANK_MOD_10 elektronického výkaznictví.
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
ms.openlocfilehash: 42a345fc48b0d87b353308060903a6b5156c0e62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915871"
---
# <span data-ttu-id="a01ab-103"><a name="CH_BANK_MOD_10">Funkce el. výkaznictví CH_BANK_MOD_10</a></span><span class="sxs-lookup"><span data-stu-id="a01ab-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a01ab-104">Funkce `CH_BANK_MOD_10` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD10 na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="a01ab-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a01ab-105">Syntax</span></span>

```
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="a01ab-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="a01ab-106">Arguments</span></span>

<span data-ttu-id="a01ab-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="a01ab-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="a01ab-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="a01ab-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="a01ab-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a01ab-109">Return values</span></span>

<span data-ttu-id="a01ab-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a01ab-110">*String*</span></span>

<span data-ttu-id="a01ab-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="a01ab-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a01ab-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="a01ab-112">Example</span></span>

<span data-ttu-id="a01ab-113">`CH_BANK_MOD_10 ("VEND-200002")` vrátí **3**.</span><span class="sxs-lookup"><span data-stu-id="a01ab-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a01ab-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a01ab-114">Additional resources</span></span>

[<span data-ttu-id="a01ab-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="a01ab-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
