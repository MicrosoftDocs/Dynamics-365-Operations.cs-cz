---
title: Funkce el. výkaznictví ISVALIDCHARACTERISO7064
description: Toto téma obsahuje obecné informace o použití funkce ISVALIDCHARACTERISO7064 elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 21962952bb3bdd016831dc5e196af27c69ecc6db
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744064"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="b1df1-103">Funkce el. výkaznictví ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="b1df1-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1df1-104">Funkce `ISVALIDCHARACTERISO7064` vrátí *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN).</span><span class="sxs-lookup"><span data-stu-id="b1df1-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="b1df1-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b1df1-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1df1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1df1-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="b1df1-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b1df1-107">Arguments</span></span>

<span data-ttu-id="b1df1-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="b1df1-108">`text`: *String*</span></span>

<span data-ttu-id="b1df1-109">Textová hodnota, která představuje IBAN.</span><span class="sxs-lookup"><span data-stu-id="b1df1-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1df1-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b1df1-110">Return values</span></span>

<span data-ttu-id="b1df1-111">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="b1df1-111">*String*</span></span>

<span data-ttu-id="b1df1-112">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="b1df1-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b1df1-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="b1df1-113">Example</span></span>

<span data-ttu-id="b1df1-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b1df1-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="b1df1-115">`ISVALIDCHARACTERISO7064 ("AT61")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="b1df1-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1df1-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b1df1-116">Additional resources</span></span>

[<span data-ttu-id="b1df1-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="b1df1-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
