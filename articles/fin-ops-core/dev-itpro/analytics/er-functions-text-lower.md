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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad971bd78fa1da17be916efcc6857aa32575f7ac
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680307"
---
# <a name="lower-er-function"></a><span data-ttu-id="0b2bd-103">Funkce elektronického výkaznictví LOWER</span><span class="sxs-lookup"><span data-stu-id="0b2bd-103">LOWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b2bd-104">Funkce `LOWER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na malá písmena.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2bd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b2bd-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="0b2bd-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0b2bd-106">Arguments</span></span>

<span data-ttu-id="0b2bd-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="0b2bd-107">`text`: *String*</span></span>

<span data-ttu-id="0b2bd-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0b2bd-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0b2bd-109">Return values</span></span>

<span data-ttu-id="0b2bd-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="0b2bd-110">*String*</span></span>

<span data-ttu-id="0b2bd-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0b2bd-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="0b2bd-112">Example</span></span>

<span data-ttu-id="0b2bd-113">`LOWER ("Sample")` vrátí **"sample"**.</span><span class="sxs-lookup"><span data-stu-id="0b2bd-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0b2bd-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0b2bd-114">Additional resources</span></span>

[<span data-ttu-id="0b2bd-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="0b2bd-115">Text functions</span></span>](er-functions-category-text.md)
