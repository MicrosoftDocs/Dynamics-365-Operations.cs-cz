---
title: Funkce elektronického výkaznictví RIGHT
description: Toto téma obsahuje obecné informace o použití funkce RIGHT elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746116"
---
# <a name="right-er-function"></a><span data-ttu-id="2ed77-103">Funkce elektronického výkaznictví RIGHT</span><span class="sxs-lookup"><span data-stu-id="2ed77-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ed77-104">Funkce `RIGHT` vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce.</span><span class="sxs-lookup"><span data-stu-id="2ed77-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ed77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ed77-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="2ed77-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="2ed77-106">Arguments</span></span>

<span data-ttu-id="2ed77-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="2ed77-107">`text`: *String*</span></span>

<span data-ttu-id="2ed77-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="2ed77-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="2ed77-109">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="2ed77-109">`number`: *Integer*</span></span>

<span data-ttu-id="2ed77-110">Počet znaků, které mají být vráceny od konce původního textu.</span><span class="sxs-lookup"><span data-stu-id="2ed77-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ed77-111">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="2ed77-111">Return values</span></span>

<span data-ttu-id="2ed77-112">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="2ed77-112">*String*</span></span>

<span data-ttu-id="2ed77-113">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="2ed77-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="2ed77-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="2ed77-114">Example</span></span>

<span data-ttu-id="2ed77-115">`RIGHT ("Sample", 3)` vrátí **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="2ed77-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ed77-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2ed77-116">Additional resources</span></span>

[<span data-ttu-id="2ed77-117">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="2ed77-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]