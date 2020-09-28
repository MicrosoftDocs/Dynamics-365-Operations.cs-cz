---
title: Funkce el. výkaznictví CHAR
description: Toto téma obsahuje obecné informace o použití funkce CHAR elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744954"
---
# <a name="char-er-function"></a><span data-ttu-id="81f46-103">Funkce el. výkaznictví CHAR</span><span class="sxs-lookup"><span data-stu-id="81f46-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81f46-104">Funkce `CHAR` vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode.</span><span class="sxs-lookup"><span data-stu-id="81f46-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="81f46-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81f46-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="81f46-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="81f46-106">Arguments</span></span>

<span data-ttu-id="81f46-107">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="81f46-107">`number`: *Integer*</span></span>

<span data-ttu-id="81f46-108">Číslo, které odpovídá požadovanému znaku.</span><span class="sxs-lookup"><span data-stu-id="81f46-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="81f46-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="81f46-109">Return values</span></span>

<span data-ttu-id="81f46-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="81f46-110">*String*</span></span>

<span data-ttu-id="81f46-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="81f46-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81f46-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="81f46-112">Usage notes</span></span>

<span data-ttu-id="81f46-113">Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu **FILE**.</span><span class="sxs-lookup"><span data-stu-id="81f46-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="81f46-114">Seznam podporovaných kódování naleznete v části [Třída kódování](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="81f46-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="81f46-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="81f46-115">Example</span></span>

<span data-ttu-id="81f46-116">`CHAR (255)` vrátí **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="81f46-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81f46-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="81f46-117">Additional resources</span></span>

[<span data-ttu-id="81f46-118">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="81f46-118">Text functions</span></span>](er-functions-category-text.md)
