---
title: Funkce elektronického výkaznictví FIRSTORNULL
description: Toto téma popisuje použití funkce FIRSTORNULL elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 075b2e064641061adf5404591a784311b6d28697
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917320"
---
# <span data-ttu-id="156eb-103"><a name="FIRSTORNULL">Funkce elektronického výkaznictví FIRSTORNULL</a></span><span class="sxs-lookup"><span data-stu-id="156eb-103"><a name="FIRSTORNULL">FIRSTORNULL ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="156eb-104">Funkce `FIRSTORNULL` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento záznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="156eb-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="156eb-105">Je-li záznam prázdný, vrátí tato funkce hodnotu typu *kontejner (záznam)* s hodnotou null.</span><span class="sxs-lookup"><span data-stu-id="156eb-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="156eb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="156eb-106">Syntax</span></span>

```
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="156eb-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="156eb-107">Arguments</span></span>

<span data-ttu-id="156eb-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="156eb-108">`list`: *Record list*</span></span>

<span data-ttu-id="156eb-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="156eb-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="156eb-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="156eb-110">Return values</span></span>

<span data-ttu-id="156eb-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="156eb-111">*Container (record)*</span></span>

<span data-ttu-id="156eb-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="156eb-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="156eb-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="156eb-113">Example</span></span>

<span data-ttu-id="156eb-114">Výraz `FIRSTORNULL(SPLIT("",1)).Value` vrátí prázdný řetězec (**""**).</span><span class="sxs-lookup"><span data-stu-id="156eb-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="156eb-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="156eb-115">Additional resources</span></span>

[<span data-ttu-id="156eb-116">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="156eb-116">List functions</span></span>](er-functions-category-list.md)
