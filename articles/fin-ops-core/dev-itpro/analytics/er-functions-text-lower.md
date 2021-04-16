---
title: Funkce elektronického výkaznictví LOWER
description: Toto téma obsahuje obecné informace o použití funkce LOWER elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: e684883d4262e4c3cd8a84d0a1c6f1d685bb650b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746284"
---
# <a name="lower-er-function"></a><span data-ttu-id="b3be0-103">Funkce elektronického výkaznictví LOWER</span><span class="sxs-lookup"><span data-stu-id="b3be0-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3be0-104">Funkce `LOWER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na malá písmena.</span><span class="sxs-lookup"><span data-stu-id="b3be0-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3be0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3be0-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="b3be0-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b3be0-106">Arguments</span></span>

<span data-ttu-id="b3be0-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="b3be0-107">`text`: *String*</span></span>

<span data-ttu-id="b3be0-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="b3be0-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3be0-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b3be0-109">Return values</span></span>

<span data-ttu-id="b3be0-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="b3be0-110">*String*</span></span>

<span data-ttu-id="b3be0-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="b3be0-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b3be0-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="b3be0-112">Example</span></span>

<span data-ttu-id="b3be0-113">`LOWER ("Sample")` vrátí **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="b3be0-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b3be0-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b3be0-114">Additional resources</span></span>

[<span data-ttu-id="b3be0-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="b3be0-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]