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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041646"
---
# <span data-ttu-id="e52b5-103"><a name="ABS">Funkce el. výkaznictví ABS</a></span><span class="sxs-lookup"><span data-stu-id="e52b5-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e52b5-104">Funkce `ABS` vrací absolutní hodnotu (modul) zadaného čísla jako hodnotu typu *reálné číslo*.</span><span class="sxs-lookup"><span data-stu-id="e52b5-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="e52b5-105">Jinými slovy, vrací číslo bez znaménka.</span><span class="sxs-lookup"><span data-stu-id="e52b5-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52b5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e52b5-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="e52b5-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e52b5-107">Arguments</span></span>

<span data-ttu-id="e52b5-108">`number`: *reálné číslo*</span><span class="sxs-lookup"><span data-stu-id="e52b5-108">`number`: *Real*</span></span>

<span data-ttu-id="e52b5-109">Číselná hodnota, ze které chceme získat modul.</span><span class="sxs-lookup"><span data-stu-id="e52b5-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="e52b5-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e52b5-110">Return values</span></span>

<span data-ttu-id="e52b5-111">*Reálný*</span><span class="sxs-lookup"><span data-stu-id="e52b5-111">*Real*</span></span>

<span data-ttu-id="e52b5-112">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="e52b5-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e52b5-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="e52b5-113">Example</span></span>

<span data-ttu-id="e52b5-114">`ABS (-1)` vrátí **1**.</span><span class="sxs-lookup"><span data-stu-id="e52b5-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e52b5-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e52b5-115">Additional resources</span></span>

[<span data-ttu-id="e52b5-116">Matematické funkce</span><span class="sxs-lookup"><span data-stu-id="e52b5-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
