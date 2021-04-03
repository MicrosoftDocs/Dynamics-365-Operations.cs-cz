---
title: Funkce elektronického výkaznictví FIRST
description: Toto téma obsahuje obecné informace o použití funkce FIRST elektronického výkaznictví.
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
ms.openlocfilehash: ec94a27776cf1069b50b5437f4d167019fdef120
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564728"
---
# <a name="first-er-function"></a><span data-ttu-id="0ae12-103">Funkce elektronického výkaznictví FIRST</span><span class="sxs-lookup"><span data-stu-id="0ae12-103">FIRST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ae12-104">Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="0ae12-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="0ae12-105">Pokud je seznam prázdný, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="0ae12-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae12-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ae12-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="0ae12-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0ae12-107">Arguments</span></span>

<span data-ttu-id="0ae12-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="0ae12-108">`list`: *Record list*</span></span>

<span data-ttu-id="0ae12-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="0ae12-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ae12-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0ae12-110">Return values</span></span>

<span data-ttu-id="0ae12-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="0ae12-111">*Container (record)*</span></span>

<span data-ttu-id="0ae12-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="0ae12-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0ae12-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="0ae12-113">Example 1</span></span>

<span data-ttu-id="0ae12-114">Výraz `FIRST(SPLIT("ABC",1)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="0ae12-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0ae12-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="0ae12-115">Example 2</span></span>

<span data-ttu-id="0ae12-116">Výraz `FIRST(SPLIT("",1)).Value` vyvolá výjimku za běhu.</span><span class="sxs-lookup"><span data-stu-id="0ae12-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ae12-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0ae12-117">Additional resources</span></span>

[<span data-ttu-id="0ae12-118">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="0ae12-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]