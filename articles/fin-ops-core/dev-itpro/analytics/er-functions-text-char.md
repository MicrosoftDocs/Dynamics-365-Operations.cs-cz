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
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915733"
---
# <span data-ttu-id="a11fe-103"><a name="CHAR">Funkce el. výkaznictví CHAR</a></span><span class="sxs-lookup"><span data-stu-id="a11fe-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a11fe-104">Funkce `CHAR` vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode.</span><span class="sxs-lookup"><span data-stu-id="a11fe-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11fe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a11fe-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="a11fe-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="a11fe-106">Arguments</span></span>

<span data-ttu-id="a11fe-107">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="a11fe-107">`number`: *Integer*</span></span>

<span data-ttu-id="a11fe-108">Číslo, které odpovídá požadovanému znaku.</span><span class="sxs-lookup"><span data-stu-id="a11fe-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="a11fe-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="a11fe-109">Return values</span></span>

<span data-ttu-id="a11fe-110">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="a11fe-110">*String*</span></span>

<span data-ttu-id="a11fe-111">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="a11fe-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a11fe-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="a11fe-112">Usage notes</span></span>

<span data-ttu-id="a11fe-113">Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu **FILE**.</span><span class="sxs-lookup"><span data-stu-id="a11fe-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="a11fe-114">Seznam podporovaných kódování naleznete v části [Třída kódování](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="a11fe-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="a11fe-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="a11fe-115">Example</span></span>

<span data-ttu-id="a11fe-116">`CHAR (255)` vrátí **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="a11fe-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a11fe-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a11fe-117">Additional resources</span></span>

[<span data-ttu-id="a11fe-118">Textové funkce</span><span class="sxs-lookup"><span data-stu-id="a11fe-118">Text functions</span></span>](er-functions-category-text.md)
