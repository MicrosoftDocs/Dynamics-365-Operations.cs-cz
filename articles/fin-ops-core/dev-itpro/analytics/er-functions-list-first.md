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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042083"
---
# <span data-ttu-id="b30db-103"><a name="FIRST">Funkce elektronického výkaznictví FIRST</a></span><span class="sxs-lookup"><span data-stu-id="b30db-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b30db-104">Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="b30db-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="b30db-105">Pokud je seznam prázdný, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="b30db-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30db-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b30db-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="b30db-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="b30db-107">Arguments</span></span>

<span data-ttu-id="b30db-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="b30db-108">`list`: *Record list*</span></span>

<span data-ttu-id="b30db-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="b30db-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b30db-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="b30db-110">Return values</span></span>

<span data-ttu-id="b30db-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="b30db-111">*Container (record)*</span></span>

<span data-ttu-id="b30db-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="b30db-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="b30db-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="b30db-113">Example 1</span></span>

<span data-ttu-id="b30db-114">Výraz `FIRST(SPLIT("ABC",1)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="b30db-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b30db-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="b30db-115">Example 2</span></span>

<span data-ttu-id="b30db-116">Výraz `FIRST(SPLIT("",1)).Value` vyvolá výjimku za běhu.</span><span class="sxs-lookup"><span data-stu-id="b30db-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b30db-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b30db-117">Additional resources</span></span>

[<span data-ttu-id="b30db-118">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="b30db-118">List functions</span></span>](er-functions-category-list.md)
