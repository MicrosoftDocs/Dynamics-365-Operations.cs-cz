---
title: Funkce el. výkaznictví NOT
description: Toto téma obsahuje obecné informace o použití funkce NOT elektronického výkaznictví.
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
ms.openlocfilehash: a518f255a4488c5ed6e007b1787e678fd88aff36
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041715"
---
# <span data-ttu-id="c2df3-103"><a name="NOT">Funkce el. výkaznictví NOT</a></span><span class="sxs-lookup"><span data-stu-id="c2df3-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2df3-104">Funkce `NOT` vrací stornovanou logickou hodnotu zadané podmínky jako *logickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="c2df3-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2df3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2df3-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="c2df3-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="c2df3-106">Arguments</span></span>

<span data-ttu-id="c2df3-107">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="c2df3-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="c2df3-108">Platný podmíněný výraz, který má být stornován.</span><span class="sxs-lookup"><span data-stu-id="c2df3-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2df3-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="c2df3-109">Return values</span></span>

<span data-ttu-id="c2df3-110">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="c2df3-110">*Boolean*</span></span>

<span data-ttu-id="c2df3-111">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="c2df3-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="c2df3-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="c2df3-112">Example</span></span>

<span data-ttu-id="c2df3-113">`NOT (TRUE)` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c2df3-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2df3-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c2df3-114">Additional resources</span></span>

[<span data-ttu-id="c2df3-115">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="c2df3-115">Logical functions</span></span>](er-functions-category-logical.md)
