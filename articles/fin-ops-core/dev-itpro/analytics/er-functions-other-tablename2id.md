---
title: Funkce el. výkaznictví TABLENAME2ID
description: Toto téma obsahuje obecné informace o použití funkce TABLENAME2ID elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681151"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="0fd5d-103">Funkce el. výkaznictví TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="0fd5d-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fd5d-104">Funkce `TABLENAME2ID` vrátí číselnou reprezentaci ID tabulky pro zadaný název tabulky jako *celočíselnou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0fd5d-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd5d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0fd5d-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="0fd5d-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0fd5d-106">Arguments</span></span>

<span data-ttu-id="0fd5d-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="0fd5d-107">`text`: *String*</span></span>

<span data-ttu-id="0fd5d-108">Textová hodnota, která představuje platný název tabulky.</span><span class="sxs-lookup"><span data-stu-id="0fd5d-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="0fd5d-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0fd5d-109">Return values</span></span>

<span data-ttu-id="0fd5d-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="0fd5d-110">*Integer*</span></span>

<span data-ttu-id="0fd5d-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="0fd5d-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0fd5d-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="0fd5d-112">Usage notes</span></span>

<span data-ttu-id="0fd5d-113">Spuštění této funkce může mít různé výsledky v různých instancích aplikace Microsoft Dynamics 365 Finance, i když je použit stejný název společnosti.</span><span class="sxs-lookup"><span data-stu-id="0fd5d-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="0fd5d-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="0fd5d-114">Example</span></span>

<span data-ttu-id="0fd5d-115">`TABLENAME2ID ("Intrastat")` vrátí **1510**.</span><span class="sxs-lookup"><span data-stu-id="0fd5d-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0fd5d-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0fd5d-116">Additional resources</span></span>

[<span data-ttu-id="0fd5d-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="0fd5d-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
