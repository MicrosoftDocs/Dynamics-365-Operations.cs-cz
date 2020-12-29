---
title: Funkce elektronického výkaznictví RIGHT
description: Toto téma obsahuje obecné informace o použití funkce RIGHT elektronického výkaznictví.
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
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682935"
---
# <a name="right-er-function"></a><span data-ttu-id="1a74f-103">Funkce elektronického výkaznictví RIGHT</span><span class="sxs-lookup"><span data-stu-id="1a74f-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a74f-104">Funkce `RIGHT` vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="1a74f-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a74f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a74f-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="1a74f-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="1a74f-106">Arguments</span></span>

<span data-ttu-id="1a74f-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="1a74f-107">`text`: *String*</span></span>

<span data-ttu-id="1a74f-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="1a74f-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="1a74f-109">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="1a74f-109">`number`: *Integer*</span></span>

<span data-ttu-id="1a74f-110">Počet znaků, které mají být vráceny od konce původního textu.</span><span class="sxs-lookup"><span data-stu-id="1a74f-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="1a74f-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="1a74f-111">Return values</span></span>

<span data-ttu-id="1a74f-112">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="1a74f-112">*String*</span></span>

<span data-ttu-id="1a74f-113">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="1a74f-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1a74f-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="1a74f-114">Example</span></span>

<span data-ttu-id="1a74f-115">`RIGHT ("Sample", 3)` vrátí **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="1a74f-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1a74f-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1a74f-116">Additional resources</span></span>

[<span data-ttu-id="1a74f-117">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="1a74f-117">Text functions</span></span>](er-functions-category-text.md)
