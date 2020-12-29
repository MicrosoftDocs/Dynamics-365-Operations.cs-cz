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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bca82cd596ba1e3ec42b3dba91ee6c4871ff8601
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686851"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="9fa3b-103">Funkce el. výkaznictví CH_BANK_MOD_10</span><span class="sxs-lookup"><span data-stu-id="9fa3b-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fa3b-104">Funkce `CH_BANK_MOD_10` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD10 na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fa3b-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="9fa3b-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9fa3b-106">Arguments</span></span>

<span data-ttu-id="9fa3b-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9fa3b-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="9fa3b-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="9fa3b-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9fa3b-109">Return values</span></span>

<span data-ttu-id="9fa3b-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="9fa3b-110">*String*</span></span>

<span data-ttu-id="9fa3b-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9fa3b-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="9fa3b-112">Example</span></span>

<span data-ttu-id="9fa3b-113">`CH_BANK_MOD_10 ("VEND-200002")` vrátí **3**.</span><span class="sxs-lookup"><span data-stu-id="9fa3b-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9fa3b-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9fa3b-114">Additional resources</span></span>

[<span data-ttu-id="9fa3b-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="9fa3b-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
