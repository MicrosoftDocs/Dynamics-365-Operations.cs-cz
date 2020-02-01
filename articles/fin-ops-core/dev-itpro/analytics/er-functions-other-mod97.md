---
title: Funkce el. výkaznictví MOD_97
description: Toto téma obsahuje obecné informace o použití funkce MOD_97 elektronického výkaznictví.
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
ms.openlocfilehash: 23e63f6b7999399fd5365c616613cbc603774d53
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916929"
---
# <span data-ttu-id="69bec-103"><a name="MOD_97">Funkce el. výkaznictví MOD_97</a></span><span class="sxs-lookup"><span data-stu-id="69bec-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69bec-104">Funkce `MOD_97` vrátí hodnotu typu *řetězec*, která představuje referenční údaj věřitele jako výraz MOD97 na základě číslic zadaného čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="69bec-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69bec-105">Syntax</span></span>

```
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="69bec-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="69bec-106">Arguments</span></span>

<span data-ttu-id="69bec-107">`invoice number digits`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="69bec-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="69bec-108">Textová hodnota, která představuje číslice čísla faktury.</span><span class="sxs-lookup"><span data-stu-id="69bec-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="69bec-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="69bec-109">Return values</span></span>

<span data-ttu-id="69bec-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="69bec-110">*String*</span></span>

<span data-ttu-id="69bec-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="69bec-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="69bec-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="69bec-112">Example</span></span>

<span data-ttu-id="69bec-113">`MOD_97 ("VEND-200002")` vrátí **"20000285"**.</span><span class="sxs-lookup"><span data-stu-id="69bec-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69bec-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="69bec-114">Additional resources</span></span>

[<span data-ttu-id="69bec-115">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="69bec-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)