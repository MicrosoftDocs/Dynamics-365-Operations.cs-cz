---
title: Funkce el. výkaznictví ISVALIDCHARACTERISO7064
description: Toto téma obsahuje obecné informace o použití funkce ISVALIDCHARACTERISO7064 elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 26300adce5f9a8a567510885577c6cfb9b1c859a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563359"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="f79f0-103">Funkce el. výkaznictví ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="f79f0-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f79f0-104">Funkce `ISVALIDCHARACTERISO7064` vrátí *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN).</span><span class="sxs-lookup"><span data-stu-id="f79f0-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="f79f0-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f79f0-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79f0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f79f0-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="f79f0-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f79f0-107">Arguments</span></span>

<span data-ttu-id="f79f0-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="f79f0-108">`text`: *String*</span></span>

<span data-ttu-id="f79f0-109">Textová hodnota, která představuje IBAN.</span><span class="sxs-lookup"><span data-stu-id="f79f0-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="f79f0-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f79f0-110">Return values</span></span>

<span data-ttu-id="f79f0-111">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="f79f0-111">*String*</span></span>

<span data-ttu-id="f79f0-112">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="f79f0-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f79f0-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="f79f0-113">Example</span></span>

<span data-ttu-id="f79f0-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="f79f0-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="f79f0-115">`ISVALIDCHARACTERISO7064 ("AT61")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="f79f0-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f79f0-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f79f0-116">Additional resources</span></span>

[<span data-ttu-id="f79f0-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="f79f0-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]