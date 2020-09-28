---
title: Funkce elektronického výkaznictví FIRST
description: Toto téma obsahuje obecné informace o použití funkce FIRST elektronického výkaznictví.
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
ms.openlocfilehash: 3ed0e0aaf29e2a67a4842d71121f1adc24f524f7
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745218"
---
# <a name="first-er-function"></a><span data-ttu-id="849a9-103">Funkce elektronického výkaznictví FIRST</span><span class="sxs-lookup"><span data-stu-id="849a9-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="849a9-104">Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="849a9-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="849a9-105">Pokud je seznam prázdný, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="849a9-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="849a9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="849a9-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="849a9-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="849a9-107">Arguments</span></span>

<span data-ttu-id="849a9-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="849a9-108">`list`: *Record list*</span></span>

<span data-ttu-id="849a9-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="849a9-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="849a9-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="849a9-110">Return values</span></span>

<span data-ttu-id="849a9-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="849a9-111">*Container (record)*</span></span>

<span data-ttu-id="849a9-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="849a9-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="849a9-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="849a9-113">Example 1</span></span>

<span data-ttu-id="849a9-114">Výraz `FIRST(SPLIT("ABC",1)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="849a9-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="849a9-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="849a9-115">Example 2</span></span>

<span data-ttu-id="849a9-116">Výraz `FIRST(SPLIT("",1)).Value` vyvolá výjimku za běhu.</span><span class="sxs-lookup"><span data-stu-id="849a9-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="849a9-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="849a9-117">Additional resources</span></span>

[<span data-ttu-id="849a9-118">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="849a9-118">List functions</span></span>](er-functions-category-list.md)
