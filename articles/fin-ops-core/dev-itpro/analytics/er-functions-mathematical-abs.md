---
title: Funkce el. výkaznictví ABS
description: Toto téma obsahuje obecné informace o použití funkce ABS elektronického výkaznictví.
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917090"
---
# <span data-ttu-id="aa08f-103"><a name="ABS">Funkce el. výkaznictví ABS</a></span><span class="sxs-lookup"><span data-stu-id="aa08f-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa08f-104">Funkce `ABS` vrací absolutní hodnotu (modul) zadaného čísla jako hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="aa08f-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="aa08f-105">Jinými slovy, vrací číslo bez znaménka.</span><span class="sxs-lookup"><span data-stu-id="aa08f-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa08f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa08f-106">Syntax</span></span>

```
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="aa08f-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="aa08f-107">Arguments</span></span>

<span data-ttu-id="aa08f-108">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="aa08f-108">`number`: *Real*</span></span>

<span data-ttu-id="aa08f-109">Číselná hodnota, ze které chceme získat modul.</span><span class="sxs-lookup"><span data-stu-id="aa08f-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="aa08f-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="aa08f-110">Return values</span></span>

<span data-ttu-id="aa08f-111">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="aa08f-111">*Real*</span></span>

<span data-ttu-id="aa08f-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="aa08f-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="aa08f-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="aa08f-113">Example</span></span>

<span data-ttu-id="aa08f-114">`ABS (-1)` vrátí **1**.</span><span class="sxs-lookup"><span data-stu-id="aa08f-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa08f-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="aa08f-115">Additional resources</span></span>

[<span data-ttu-id="aa08f-116">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="aa08f-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
