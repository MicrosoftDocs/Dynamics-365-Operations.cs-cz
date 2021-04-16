---
title: Funkce el. výkaznictví NOT
description: Toto téma obsahuje obecné informace o použití funkce NOT elektronického výkaznictví.
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
ms.openlocfilehash: 7c10ed61b97dcd4d4a66a530bb3d08c539659233
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751698"
---
# <a name="not-er-function"></a><span data-ttu-id="9ae22-103">Funkce el. výkaznictví NOT</span><span class="sxs-lookup"><span data-stu-id="9ae22-103">NOT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ae22-104">Funkce `NOT` vrací stornovanou logickou hodnotu zadané podmínky jako *logickou hodnotu*.</span><span class="sxs-lookup"><span data-stu-id="9ae22-104">The `NOT` function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ae22-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ae22-105">Syntax</span></span>

```vb
NOT (condition)
```

## <a name="arguments"></a><span data-ttu-id="9ae22-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9ae22-106">Arguments</span></span>

<span data-ttu-id="9ae22-107">`condition`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="9ae22-107">`condition`: *Boolean*</span></span>

<span data-ttu-id="9ae22-108">Platný podmíněný výraz, který má být stornován.</span><span class="sxs-lookup"><span data-stu-id="9ae22-108">A valid conditional expression that must be reversed.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ae22-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9ae22-109">Return values</span></span>

<span data-ttu-id="9ae22-110">*Logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="9ae22-110">*Boolean*</span></span>

<span data-ttu-id="9ae22-111">Výsledná *logická hodnota*.</span><span class="sxs-lookup"><span data-stu-id="9ae22-111">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="9ae22-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="9ae22-112">Example</span></span>

<span data-ttu-id="9ae22-113">`NOT (TRUE)` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="9ae22-113">`NOT (TRUE)` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ae22-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9ae22-114">Additional resources</span></span>

[<span data-ttu-id="9ae22-115">Logické funkce</span><span class="sxs-lookup"><span data-stu-id="9ae22-115">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]