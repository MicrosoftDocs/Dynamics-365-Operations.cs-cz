---
title: Funkce elektronického výkaznictví LOWER
description: Toto téma obsahuje obecné informace o použití funkce LOWER elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: e507a17f5125a3cba0d2434a1aaec0f04f0cd388
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562776"
---
# <a name="lower-er-function"></a><span data-ttu-id="5eb32-103">Funkce elektronického výkaznictví LOWER</span><span class="sxs-lookup"><span data-stu-id="5eb32-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5eb32-104">Funkce `LOWER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na malá písmena.</span><span class="sxs-lookup"><span data-stu-id="5eb32-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb32-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5eb32-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="5eb32-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5eb32-106">Arguments</span></span>

<span data-ttu-id="5eb32-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5eb32-107">`text`: *String*</span></span>

<span data-ttu-id="5eb32-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="5eb32-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5eb32-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5eb32-109">Return values</span></span>

<span data-ttu-id="5eb32-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="5eb32-110">*String*</span></span>

<span data-ttu-id="5eb32-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="5eb32-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5eb32-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="5eb32-112">Example</span></span>

<span data-ttu-id="5eb32-113">`LOWER ("Sample")` vrátí **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="5eb32-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5eb32-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5eb32-114">Additional resources</span></span>

[<span data-ttu-id="5eb32-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="5eb32-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]