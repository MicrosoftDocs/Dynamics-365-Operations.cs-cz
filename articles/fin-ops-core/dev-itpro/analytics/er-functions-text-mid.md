---
title: Funkce el. výkaznictví MID
description: Toto téma obsahuje obecné informace o použití funkce MID elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 1d8a7d2e9beb0fc8724d26de0acaf1d61e3834c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680283"
---
# <a name="mid-er-function"></a><span data-ttu-id="657f5-103">Funkce el. výkaznictví MID</span><span class="sxs-lookup"><span data-stu-id="657f5-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="657f5-104">Funkce `MID` vrátí hodnotu typu *řetězec*, která představuje zadaný počet znaků ze zadaného řetězce počínaje zadanou pozicí.</span><span class="sxs-lookup"><span data-stu-id="657f5-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="657f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="657f5-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="657f5-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="657f5-106">Arguments</span></span>

<span data-ttu-id="657f5-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="657f5-107">`text`: *String*</span></span>

<span data-ttu-id="657f5-108">Hodnota typu *řetězec* určující text, ze kterého se budou vracet znaky.</span><span class="sxs-lookup"><span data-stu-id="657f5-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="657f5-109">`starting position`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="657f5-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="657f5-110">Hodnota typu *celé číslo*, která určuje pozici prvního znaku, který má být vrácen ze zadaného textu.</span><span class="sxs-lookup"><span data-stu-id="657f5-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="657f5-111">`number of characters`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="657f5-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="657f5-112">Hodnota typu *celé číslo*, která určuje počet znaků, které mají být vráceny počínaje zadanou počáteční pozicí.</span><span class="sxs-lookup"><span data-stu-id="657f5-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="657f5-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="657f5-113">Return values</span></span>

<span data-ttu-id="657f5-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="657f5-114">*String*</span></span>

<span data-ttu-id="657f5-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="657f5-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="657f5-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="657f5-116">Usage notes</span></span>

<span data-ttu-id="657f5-117">Pokud je hodnota argumentu `starting position` menší než 0 (nula), jsou vracené znaky počítány od první pozice v zadaném řetězci.</span><span class="sxs-lookup"><span data-stu-id="657f5-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="657f5-118">Pokud hodnota argumentu `starting position` přesahuje délku zadaného řetězce, je vrácen prázdný řetězec.</span><span class="sxs-lookup"><span data-stu-id="657f5-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="657f5-119">Příklad</span><span class="sxs-lookup"><span data-stu-id="657f5-119">Example</span></span>

<span data-ttu-id="657f5-120">`MID ("Sample", 2, 3)` vrátí hodnotu **"amp"**.</span><span class="sxs-lookup"><span data-stu-id="657f5-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="657f5-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="657f5-121">Additional resources</span></span>

[<span data-ttu-id="657f5-122">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="657f5-122">Text functions</span></span>](er-functions-category-text.md)
