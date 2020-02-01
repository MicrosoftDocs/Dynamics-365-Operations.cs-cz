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
ms.openlocfilehash: 211891a0ad5dc6152ce8d980bcd40a9a6bc7e3e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917343"
---
# <span data-ttu-id="4469b-103"><a name="FIRST">Funkce elektronického výkaznictví FIRST</a></span><span class="sxs-lookup"><span data-stu-id="4469b-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4469b-104">Funkce `FIRST` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento seznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="4469b-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="4469b-105">Pokud je seznam prázdný, vyvolá tato funkce výjimku.</span><span class="sxs-lookup"><span data-stu-id="4469b-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="4469b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4469b-106">Syntax</span></span>

```
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="4469b-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="4469b-107">Arguments</span></span>

<span data-ttu-id="4469b-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="4469b-108">`list`: *Record list*</span></span>

<span data-ttu-id="4469b-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="4469b-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4469b-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="4469b-110">Return values</span></span>

<span data-ttu-id="4469b-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="4469b-111">*Container (record)*</span></span>

<span data-ttu-id="4469b-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="4469b-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="4469b-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="4469b-113">Example 1</span></span>

<span data-ttu-id="4469b-114">Výraz `FIRST(SPLIT("ABC",1)).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="4469b-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4469b-115">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="4469b-115">Example 2</span></span>

<span data-ttu-id="4469b-116">Výraz `FIRST(SPLIT("",1)).Value` vyvolá výjimku za běhu.</span><span class="sxs-lookup"><span data-stu-id="4469b-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4469b-117">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4469b-117">Additional resources</span></span>

[<span data-ttu-id="4469b-118">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="4469b-118">List functions</span></span>](er-functions-category-list.md)