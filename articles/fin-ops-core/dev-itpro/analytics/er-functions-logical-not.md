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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916032"
---
# <span data-ttu-id="255df-103"><a name="NOT">Funkce el. výkaznictví NOT</a></span><span class="sxs-lookup"><span data-stu-id="255df-103"><a name="NOT">NOT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="255df-104">Funkce `NOT` vrací stornovanou logickou hodnotu zadané podmínky jako *logickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="255df-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="255df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="255df-105">Syntax</span></span>

```
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="255df-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="255df-106">Arguments</span></span>

<span data-ttu-id="255df-107">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="255df-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="255df-108">Platný podmíněný výraz, který má být stornován.</span><span class="sxs-lookup"><span data-stu-id="255df-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="255df-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="255df-109">Return values</span></span>

<span data-ttu-id="255df-110">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="255df-110">*Boolean*</span></span>

<span data-ttu-id="255df-111">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="255df-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="255df-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="255df-112">Example</span></span>

<span data-ttu-id="255df-113">`NOT (TRUE)` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="255df-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="255df-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="255df-114">Additional resources</span></span>

[<span data-ttu-id="255df-115">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="255df-115">Logical functions</span></span>](er-functions-category-logical.md)
