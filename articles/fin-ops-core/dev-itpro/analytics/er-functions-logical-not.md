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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2308ab4d222863312441b3f17559ac4d3afbfb29
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686947"
---
# <a name="not-er-function"></a><span data-ttu-id="ff2da-103">Funkce el. výkaznictví NOT</span><span class="sxs-lookup"><span data-stu-id="ff2da-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ff2da-104">Funkce `NOT` vrací stornovanou logickou hodnotu zadané podmínky jako *logickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="ff2da-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff2da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff2da-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="ff2da-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="ff2da-106">Arguments</span></span>

<span data-ttu-id="ff2da-107">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="ff2da-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="ff2da-108">Platný podmíněný výraz, který má být stornován.</span><span class="sxs-lookup"><span data-stu-id="ff2da-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="ff2da-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ff2da-109">Return values</span></span>

<span data-ttu-id="ff2da-110">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="ff2da-110">*Boolean*</span></span>

<span data-ttu-id="ff2da-111">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="ff2da-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="ff2da-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="ff2da-112">Example</span></span>

<span data-ttu-id="ff2da-113">`NOT (TRUE)` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="ff2da-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ff2da-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ff2da-114">Additional resources</span></span>

[<span data-ttu-id="ff2da-115">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="ff2da-115">Logical functions</span></span>](er-functions-category-logical.md)
