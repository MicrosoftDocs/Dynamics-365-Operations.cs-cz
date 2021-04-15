---
title: Funkce el. výkaznictví ABS
description: Toto téma obsahuje obecné informace o použití funkce ABS elektronického výkaznictví.
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753137"
---
# <a name="abs-er-function"></a><span data-ttu-id="a609a-103">Funkce el. výkaznictví ABS</span><span class="sxs-lookup"><span data-stu-id="a609a-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a609a-104">Funkce `ABS` vrací absolutní hodnotu (modul) zadaného čísla jako hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="a609a-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="a609a-105">Jinými slovy, vrací číslo bez znaménka.</span><span class="sxs-lookup"><span data-stu-id="a609a-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="a609a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a609a-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="a609a-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="a609a-107">Arguments</span></span>

<span data-ttu-id="a609a-108">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="a609a-108">`number`: *Real*</span></span>

<span data-ttu-id="a609a-109">Číselná hodnota, ze které chceme získat modul.</span><span class="sxs-lookup"><span data-stu-id="a609a-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="a609a-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a609a-110">Return values</span></span>

<span data-ttu-id="a609a-111">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="a609a-111">*Real*</span></span>

<span data-ttu-id="a609a-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="a609a-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="a609a-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="a609a-113">Example</span></span>

<span data-ttu-id="a609a-114">`ABS (-1)` vrátí **1**.</span><span class="sxs-lookup"><span data-stu-id="a609a-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a609a-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a609a-115">Additional resources</span></span>

[<span data-ttu-id="a609a-116">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="a609a-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]