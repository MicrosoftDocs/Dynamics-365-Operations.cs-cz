---
title: Funkce elektronického výkaznictví EMPTYLIST
description: Toto téma obsahuje obecné informace o použití funkce EMPTYLIST elektronického výkaznictví.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559193"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="34bbd-103">Funkce elektronického výkaznictví EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="34bbd-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34bbd-104">Funkce `EMPTYLIST` vrátí prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.</span><span class="sxs-lookup"><span data-stu-id="34bbd-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bbd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34bbd-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="34bbd-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="34bbd-106">Arguments</span></span>

<span data-ttu-id="34bbd-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="34bbd-107">`list`: *Record list*</span></span>

<span data-ttu-id="34bbd-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="34bbd-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="34bbd-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="34bbd-109">Return values</span></span>

<span data-ttu-id="34bbd-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="34bbd-110">*Record list*</span></span>

<span data-ttu-id="34bbd-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="34bbd-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="34bbd-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="34bbd-112">Example</span></span>

<span data-ttu-id="34bbd-113">`EMPTYLIST (SPLIT ("abc", 1))` vrátí nový prázdný seznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`, který je používán.</span><span class="sxs-lookup"><span data-stu-id="34bbd-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34bbd-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="34bbd-114">Additional resources</span></span>

[<span data-ttu-id="34bbd-115">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="34bbd-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]