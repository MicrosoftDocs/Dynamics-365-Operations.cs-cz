---
title: Funkce el. výkaznictví CHAR
description: Toto téma obsahuje obecné informace o použití funkce CHAR elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a621328817171be7df0622507c84f5c6f6fe90a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746428"
---
# <a name="char-er-function"></a><span data-ttu-id="5538c-103">Funkce el. výkaznictví CHAR</span><span class="sxs-lookup"><span data-stu-id="5538c-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5538c-104">Funkce `CHAR` vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode.</span><span class="sxs-lookup"><span data-stu-id="5538c-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5538c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5538c-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="5538c-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="5538c-106">Arguments</span></span>

<span data-ttu-id="5538c-107">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="5538c-107">`number`: *Integer*</span></span>

<span data-ttu-id="5538c-108">Číslo, které odpovídá požadovanému znaku.</span><span class="sxs-lookup"><span data-stu-id="5538c-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="5538c-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="5538c-109">Return values</span></span>

<span data-ttu-id="5538c-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="5538c-110">*String*</span></span>

<span data-ttu-id="5538c-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="5538c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5538c-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="5538c-112">Usage notes</span></span>

<span data-ttu-id="5538c-113">Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu **FILE**.</span><span class="sxs-lookup"><span data-stu-id="5538c-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="5538c-114">Seznam podporovaných kódování naleznete v části [Třída kódování](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="5538c-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="5538c-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="5538c-115">Example</span></span>

<span data-ttu-id="5538c-116">`CHAR (255)` vrátí **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="5538c-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5538c-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5538c-117">Additional resources</span></span>

[<span data-ttu-id="5538c-118">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="5538c-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]