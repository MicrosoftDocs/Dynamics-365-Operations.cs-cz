---
title: Funkce el. výkaznictví PADLEFT
description: Toto téma obsahuje obecné informace o použití funkce PADLEFT elektronického výkaznictví.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916768"
---
# <span data-ttu-id="fd550-103"><a name="PADLEFT">Funkce el. výkaznictví PADLEFT</a></span><span class="sxs-lookup"><span data-stu-id="fd550-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd550-104">Funkce `PADLEFT` vrátí hodnotu typu *řetězec* zadané délky, kde je začátek zadaného řetězce odsazen určenými znaky.</span><span class="sxs-lookup"><span data-stu-id="fd550-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd550-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fd550-105">Syntax</span></span>

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="fd550-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="fd550-106">Arguments</span></span>

<span data-ttu-id="fd550-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fd550-107">`text`: *String*</span></span>

<span data-ttu-id="fd550-108">Hodnota typu *řetězec*, která představuje původní text.</span><span class="sxs-lookup"><span data-stu-id="fd550-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="fd550-109">`length`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="fd550-109">`length`: *Integer*</span></span>

<span data-ttu-id="fd550-110">*Celočíselná* hodnota, která představuje konečný počet znaků odsazeného řetězce.</span><span class="sxs-lookup"><span data-stu-id="fd550-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="fd550-111">`padding chars`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="fd550-111">`padding chars`: *String*</span></span>

<span data-ttu-id="fd550-112">Znaky, které mají být použity pro odsazení.</span><span class="sxs-lookup"><span data-stu-id="fd550-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd550-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="fd550-113">Return values</span></span>

<span data-ttu-id="fd550-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="fd550-114">*String*</span></span>

<span data-ttu-id="fd550-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="fd550-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fd550-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="fd550-116">Example</span></span>

<span data-ttu-id="fd550-117">`PADLEFT ("1234", 10, "`&nbsp;`")` vrátí textový řetězec **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span><span class="sxs-lookup"><span data-stu-id="fd550-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fd550-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fd550-118">Additional resources</span></span>

[<span data-ttu-id="fd550-119">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="fd550-119">Text functions</span></span>](er-functions-category-text.md)