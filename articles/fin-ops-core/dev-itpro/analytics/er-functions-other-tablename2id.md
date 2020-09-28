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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9f9e38f46df8a93b5cb16b8d0d5e5afbff8558a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743992"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="b1e05-103">Funkce el. výkaznictví TABLENAME2ID</span><span class="sxs-lookup"><span data-stu-id="b1e05-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e05-104">Funkce `TABLENAME2ID` vrátí číselnou reprezentaci ID tabulky pro zadaný název tabulky jako *celočíselnou* hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b1e05-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1e05-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="b1e05-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b1e05-106">Arguments</span></span>

<span data-ttu-id="b1e05-107">`text`: *řetězec*</span><span class="sxs-lookup"><span data-stu-id="b1e05-107">`text`: *String*</span></span>

<span data-ttu-id="b1e05-108">Textová hodnota, která představuje platný název tabulky.</span><span class="sxs-lookup"><span data-stu-id="b1e05-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1e05-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b1e05-109">Return values</span></span>

<span data-ttu-id="b1e05-110">*Celé číslo*</span><span class="sxs-lookup"><span data-stu-id="b1e05-110">*Integer*</span></span>

<span data-ttu-id="b1e05-111">Výsledná číselná hodnota.</span><span class="sxs-lookup"><span data-stu-id="b1e05-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1e05-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="b1e05-112">Usage notes</span></span>

<span data-ttu-id="b1e05-113">Spuštění této funkce může mít různé výsledky v různých instancích aplikace Microsoft Dynamics 365 Finance, i když je použit stejný název společnosti.</span><span class="sxs-lookup"><span data-stu-id="b1e05-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="b1e05-114">Příklad</span><span class="sxs-lookup"><span data-stu-id="b1e05-114">Example</span></span>

<span data-ttu-id="b1e05-115">`TABLENAME2ID ("Intrastat")` vrátí **1510**.</span><span class="sxs-lookup"><span data-stu-id="b1e05-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1e05-116">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b1e05-116">Additional resources</span></span>

[<span data-ttu-id="b1e05-117">Další funkce (konkrétní pro obchodní domény)</span><span class="sxs-lookup"><span data-stu-id="b1e05-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
