---
title: Funkce el. výkaznictví TRANSLATE
description: Toto téma obsahuje obecné informace o použití funkce TRANSLATE elektronického výkaznictví.
author: NickSelin
ms.date: 04/02/2020
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
ms.openlocfilehash: 7e4d6417757e27190ab7cabf2bf01243bb87b55c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746066"
---
# <a name="translate-er-function"></a><span data-ttu-id="cdc39-103">Funkce el. výkaznictví TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="cdc39-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdc39-104">Funkce `TRANSLATE` vrací *řetězcovou* hodnotu, která obsahuje výsledek nahrazení znaku zadaného textu znaky jiné zadané sady.</span><span class="sxs-lookup"><span data-stu-id="cdc39-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdc39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdc39-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="cdc39-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="cdc39-106">Arguments</span></span>

<span data-ttu-id="cdc39-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="cdc39-107">`text`: *String*</span></span>

<span data-ttu-id="cdc39-108">Platná cesta ke zdroji dat typu *řetězec*.</span><span class="sxs-lookup"><span data-stu-id="cdc39-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="cdc39-109">`pattern`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="cdc39-109">`pattern`: *String*</span></span>

<span data-ttu-id="cdc39-110">Text, který má být nahrazen.</span><span class="sxs-lookup"><span data-stu-id="cdc39-110">The text that must be replaced.</span></span>

<span data-ttu-id="cdc39-111">`replacement`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="cdc39-111">`replacement`: *String*</span></span>

<span data-ttu-id="cdc39-112">Text, který má být použit jako náhrada.</span><span class="sxs-lookup"><span data-stu-id="cdc39-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="cdc39-113">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="cdc39-113">Return values</span></span>

<span data-ttu-id="cdc39-114">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="cdc39-114">*String*</span></span>

<span data-ttu-id="cdc39-115">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="cdc39-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cdc39-116">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="cdc39-116">Usage notes</span></span>

<span data-ttu-id="cdc39-117">Funkce `TRANSLATE` nahradí vždy jeden znak.</span><span class="sxs-lookup"><span data-stu-id="cdc39-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="cdc39-118">Funkce nahradí první znak argumentu `text` prvním znakem argumentu `pattern` a poté druhým znakem a následuje stejný tok až do dokončení.</span><span class="sxs-lookup"><span data-stu-id="cdc39-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="cdc39-119">Pokud se znak z argumentů `text` a `pattern` shoduje, je nahrazen znakem z argumentu `replacement`, který se nachází ve stejné pozici jako znak z argumentu `pattern`.</span><span class="sxs-lookup"><span data-stu-id="cdc39-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="cdc39-120">Pokud se v argumentu `pattern` několikrát objevuje znak, použije se mapování argumentů `replacement`, které odpovídá prvnímu výskytu tohoto znaku.</span><span class="sxs-lookup"><span data-stu-id="cdc39-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="cdc39-121">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="cdc39-121">Example 1</span></span>

<span data-ttu-id="cdc39-122">`TRANSLATE ("abcdef", "cd", "GH")` nahradí znak **"c"** zadaného textu **“abcdef”** znakem **"G"** textu `replacement` z následujích důvodů:</span><span class="sxs-lookup"><span data-stu-id="cdc39-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="cdc39-123">Znak **"c"** je uveden v textu `pattern` v první pozici.</span><span class="sxs-lookup"><span data-stu-id="cdc39-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="cdc39-124">První pozice textu `replacement` obsahuje znak **"G"**.</span><span class="sxs-lookup"><span data-stu-id="cdc39-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="cdc39-125">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="cdc39-125">Example 2</span></span>

<span data-ttu-id="cdc39-126">`TRANSLATE ("abcdef", "ccd", "GH")` vrátí **"abGdef"**.</span><span class="sxs-lookup"><span data-stu-id="cdc39-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="cdc39-127">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="cdc39-127">Example 3</span></span>

<span data-ttu-id="cdc39-128">`TRANSLATE ("abccba", "abc", "123")` vrátí **"123321"**.</span><span class="sxs-lookup"><span data-stu-id="cdc39-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cdc39-129">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="cdc39-129">Additional resources</span></span>

[<span data-ttu-id="cdc39-130">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="cdc39-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]