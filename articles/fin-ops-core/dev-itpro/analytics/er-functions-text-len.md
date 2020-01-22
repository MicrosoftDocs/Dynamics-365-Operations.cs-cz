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
ms.openlocfilehash: d6f2a661dd3a85c658ff85f5886d98f665e28718
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915572"
---
# <span data-ttu-id="895f6-103"><a name="LEN">Funkce el. výkaznictví LEN</a></span><span class="sxs-lookup"><span data-stu-id="895f6-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="895f6-104">Funkce `LEN` vrátí počet znaků v zadaném řetězci jako *celočíselnou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="895f6-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="895f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="895f6-105">Syntax</span></span>

```
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="895f6-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="895f6-106">Arguments</span></span>

<span data-ttu-id="895f6-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="895f6-107">`text`: *String*</span></span>

<span data-ttu-id="895f6-108">Hodnota typu *řetězec*, která představuje samotný text.</span><span class="sxs-lookup"><span data-stu-id="895f6-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="895f6-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="895f6-109">Return values</span></span>

<span data-ttu-id="895f6-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="895f6-110">*Integer*</span></span>

<span data-ttu-id="895f6-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="895f6-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="895f6-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="895f6-112">Example</span></span>

<span data-ttu-id="895f6-113">`LEN ("Sample")` vrátí **6**.</span><span class="sxs-lookup"><span data-stu-id="895f6-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="895f6-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="895f6-114">Additional resources</span></span>

[<span data-ttu-id="895f6-115">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="895f6-115">Text functions</span></span>](er-functions-category-text.md)
