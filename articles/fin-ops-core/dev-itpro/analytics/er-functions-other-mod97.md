---
title: Funkce el. výkaznictví MOD_97
description: Toto téma obsahuje obecné informace o použití funkce MOD_97 elektronického výkaznictví.
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
ms.openlocfilehash: 1054407addaf6f7c2a7d2f72bf1479e9dc374389
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749158"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="15f5b-103">Funkce el. výkaznictví MOD_97</span><span class="sxs-lookup"><span data-stu-id="15f5b-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15f5b-104">Funkce `MOD_97` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="15f5b-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="15f5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15f5b-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="15f5b-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="15f5b-106">Arguments</span></span>

<span data-ttu-id="15f5b-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="15f5b-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="15f5b-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="15f5b-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="15f5b-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="15f5b-109">Return values</span></span>

<span data-ttu-id="15f5b-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="15f5b-110">*String*</span></span>

<span data-ttu-id="15f5b-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="15f5b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="15f5b-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="15f5b-112">Example</span></span>

<span data-ttu-id="15f5b-113">`MOD_97 ("VEND-200002")` vrátí **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="15f5b-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15f5b-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="15f5b-114">Additional resources</span></span>

[<span data-ttu-id="15f5b-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="15f5b-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]