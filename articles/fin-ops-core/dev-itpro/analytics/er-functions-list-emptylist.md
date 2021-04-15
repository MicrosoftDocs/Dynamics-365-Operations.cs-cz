---
title: Funkce elektronického výkaznictví EMPTYLIST
description: Toto téma obsahuje obecné informace o použití funkce EMPTYLIST elektronického výkaznictví.
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746668"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="9c745-103">Funkce elektronického výkaznictví EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="9c745-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c745-104">Funkce `EMPTYLIST` vrátí prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.</span><span class="sxs-lookup"><span data-stu-id="9c745-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c745-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9c745-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="9c745-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="9c745-106">Arguments</span></span>

<span data-ttu-id="9c745-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="9c745-107">`list`: *Record list*</span></span>

<span data-ttu-id="9c745-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="9c745-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c745-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="9c745-109">Return values</span></span>

<span data-ttu-id="9c745-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="9c745-110">*Record list*</span></span>

<span data-ttu-id="9c745-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="9c745-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="9c745-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="9c745-112">Example</span></span>

<span data-ttu-id="9c745-113">`EMPTYLIST (SPLIT ("abc", 1))` vrátí nový prázdný seznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`, který je používán.</span><span class="sxs-lookup"><span data-stu-id="9c745-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c745-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9c745-114">Additional resources</span></span>

[<span data-ttu-id="9c745-115">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="9c745-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]