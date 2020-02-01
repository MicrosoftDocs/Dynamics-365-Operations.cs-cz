---
title: Funkce el. výkaznictví LEFT
description: Toto téma obsahuje obecné informace o použití funkce LEFT elektronického výkaznictví.
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
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915641"
---
# <span data-ttu-id="9ed90-103"><a name="LEFT">Funkce el. výkaznictví LEFT</a></span><span class="sxs-lookup"><span data-stu-id="9ed90-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ed90-104">Funkce `LEFT` vrátí hodnotu typu *řetězec*, která představuje zadaný počet znaků od počátku zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="9ed90-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ed90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ed90-105">Syntax</span></span>

```
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="9ed90-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9ed90-106">Arguments</span></span>

<span data-ttu-id="9ed90-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="9ed90-107">`text`: *String*</span></span>

<span data-ttu-id="9ed90-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="9ed90-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="9ed90-109">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="9ed90-109">`number`: *Integer*</span></span>

<span data-ttu-id="9ed90-110">Počet znaků, které mají být vráceny od začátku původního textu.</span><span class="sxs-lookup"><span data-stu-id="9ed90-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="9ed90-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9ed90-111">Return values</span></span>

<span data-ttu-id="9ed90-112">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="9ed90-112">*String*</span></span>

<span data-ttu-id="9ed90-113">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="9ed90-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="9ed90-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="9ed90-114">Example</span></span>

<span data-ttu-id="9ed90-115">`LEFT ("Sample", 3)` vrátí **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="9ed90-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9ed90-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9ed90-116">Additional resources</span></span>

[<span data-ttu-id="9ed90-117">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="9ed90-117">Text functions</span></span>](er-functions-category-text.md)