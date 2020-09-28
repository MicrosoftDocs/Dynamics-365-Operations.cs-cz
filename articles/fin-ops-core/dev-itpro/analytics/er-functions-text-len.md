---
title: Funkce el. výkaznictví LEN
description: Toto téma obsahuje obecné informace o použití funkce LEN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: e51e181de53cd185679110e99b9f89695bacdf92
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744256"
---
# <a name="len-er-function"></a><span data-ttu-id="086e5-103">Funkce el. výkaznictví LEN</span><span class="sxs-lookup"><span data-stu-id="086e5-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="086e5-104">Funkce `LEN` vrátí počet znaků v zadaném řetězci jako *celočíselnou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="086e5-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="086e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="086e5-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="086e5-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="086e5-106">Arguments</span></span>

<span data-ttu-id="086e5-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="086e5-107">`text`: *String*</span></span>

<span data-ttu-id="086e5-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="086e5-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="086e5-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="086e5-109">Return values</span></span>

<span data-ttu-id="086e5-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="086e5-110">*Integer*</span></span>

<span data-ttu-id="086e5-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="086e5-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="086e5-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="086e5-112">Example</span></span>

<span data-ttu-id="086e5-113">`LEN ("Sample")` vrátí **6**.</span><span class="sxs-lookup"><span data-stu-id="086e5-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="086e5-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="086e5-114">Additional resources</span></span>

[<span data-ttu-id="086e5-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="086e5-115">Text functions</span></span>](er-functions-category-text.md)
