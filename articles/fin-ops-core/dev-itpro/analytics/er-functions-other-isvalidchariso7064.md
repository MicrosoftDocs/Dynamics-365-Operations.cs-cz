---
title: Funkce el. výkaznictví ISVALIDCHARACTERISO7064
description: Toto téma obsahuje obecné informace o použití funkce ISVALIDCHARACTERISO7064 elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: 1f102a6a3eafe3b066101370b94fa2f17ad3ad8b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748286"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="83447-103">Funkce el. výkaznictví ISVALIDCHARACTERISO7064</span><span class="sxs-lookup"><span data-stu-id="83447-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83447-104">Funkce `ISVALIDCHARACTERISO7064` vrátí *logickou hodnotu* **TRUE**, pokud zadaný řetězec představuje platné mezinárodní číslo bankovního účtu (IBAN).</span><span class="sxs-lookup"><span data-stu-id="83447-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="83447-105">V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="83447-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="83447-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83447-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="83447-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="83447-107">Arguments</span></span>

<span data-ttu-id="83447-108">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="83447-108">`text`: *String*</span></span>

<span data-ttu-id="83447-109">Textová hodnota, která představuje IBAN.</span><span class="sxs-lookup"><span data-stu-id="83447-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="83447-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="83447-110">Return values</span></span>

<span data-ttu-id="83447-111">*Řetězec*</span><span class="sxs-lookup"><span data-stu-id="83447-111">*String*</span></span>

<span data-ttu-id="83447-112">Výsledná textová hodnota.</span><span class="sxs-lookup"><span data-stu-id="83447-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="83447-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="83447-113">Example</span></span>

<span data-ttu-id="83447-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` vrátí **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="83447-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="83447-115">`ISVALIDCHARACTERISO7064 ("AT61")` vrátí **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="83447-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83447-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="83447-116">Additional resources</span></span>

[<span data-ttu-id="83447-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="83447-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]