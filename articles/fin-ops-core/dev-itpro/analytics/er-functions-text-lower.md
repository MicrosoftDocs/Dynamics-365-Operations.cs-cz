---
title: Funkce elektronického výkaznictví LOWER
description: Toto téma obsahuje obecné informace o použití funkce LOWER elektronického výkaznictví.
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
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745674"
---
# <a name="lower-er-function"></a><span data-ttu-id="bbc55-103">Funkce elektronického výkaznictví LOWER</span><span class="sxs-lookup"><span data-stu-id="bbc55-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbc55-104">Funkce `LOWER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na malá písmena.</span><span class="sxs-lookup"><span data-stu-id="bbc55-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbc55-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bbc55-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="bbc55-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="bbc55-106">Arguments</span></span>

<span data-ttu-id="bbc55-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="bbc55-107">`text`: *String*</span></span>

<span data-ttu-id="bbc55-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="bbc55-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbc55-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="bbc55-109">Return values</span></span>

<span data-ttu-id="bbc55-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="bbc55-110">*String*</span></span>

<span data-ttu-id="bbc55-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="bbc55-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="bbc55-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="bbc55-112">Example</span></span>

<span data-ttu-id="bbc55-113">`LOWER ("Sample")` vrátí **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="bbc55-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbc55-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="bbc55-114">Additional resources</span></span>

[<span data-ttu-id="bbc55-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="bbc55-115">Text functions</span></span>](er-functions-category-text.md)
