---
title: Funkce elektronického výkaznictví RIGHT
description: Toto téma obsahuje obecné informace o použití funkce RIGHT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570233"
---
# <a name="right-er-function"></a><span data-ttu-id="5b416-103">Funkce elektronického výkaznictví RIGHT</span><span class="sxs-lookup"><span data-stu-id="5b416-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b416-104">Funkce `RIGHT` vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="5b416-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b416-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b416-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5b416-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5b416-106">Arguments</span></span>

<span data-ttu-id="5b416-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="5b416-107">`text`: *String*</span></span>

<span data-ttu-id="5b416-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="5b416-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5b416-109">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="5b416-109">`number`: *Integer*</span></span>

<span data-ttu-id="5b416-110">Počet znaků, které mají být vráceny od konce původního textu.</span><span class="sxs-lookup"><span data-stu-id="5b416-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b416-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5b416-111">Return values</span></span>

<span data-ttu-id="5b416-112">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="5b416-112">*String*</span></span>

<span data-ttu-id="5b416-113">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="5b416-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5b416-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="5b416-114">Example</span></span>

<span data-ttu-id="5b416-115">`RIGHT ("Sample", 3)` vrátí **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="5b416-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b416-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5b416-116">Additional resources</span></span>

[<span data-ttu-id="5b416-117">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="5b416-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]