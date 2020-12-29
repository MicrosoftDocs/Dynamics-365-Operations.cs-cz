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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680655"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="8d347-103">Funkce el. výkaznictví ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="8d347-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d347-104">Funkce `ISVALIDCHARACTERISO7064` vrátí *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN).</span><span class="sxs-lookup"><span data-stu-id="8d347-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="8d347-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8d347-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d347-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d347-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="8d347-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="8d347-107">Arguments</span></span>

<span data-ttu-id="8d347-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="8d347-108">`text`: *String*</span></span>

<span data-ttu-id="8d347-109">Textová hodnota, která představuje IBAN.</span><span class="sxs-lookup"><span data-stu-id="8d347-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d347-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="8d347-110">Return values</span></span>

<span data-ttu-id="8d347-111">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="8d347-111">*String*</span></span>

<span data-ttu-id="8d347-112">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="8d347-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8d347-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="8d347-113">Example</span></span>

<span data-ttu-id="8d347-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="8d347-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="8d347-115">`ISVALIDCHARACTERISO7064 ("AT61")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="8d347-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d347-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8d347-116">Additional resources</span></span>

[<span data-ttu-id="8d347-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="8d347-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
