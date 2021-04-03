---
title: Funkce elektronického výkaznictví FIRSTORNULL
description: Toto téma popisuje použití funkce FIRSTORNULL elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 53284333507ef1264d3eb66b0c7141eb69f32392
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564618"
---
# <a name="firstornull-er-function"></a><span data-ttu-id="deb63-103">Funkce elektronického výkaznictví FIRSTORNULL</span><span class="sxs-lookup"><span data-stu-id="deb63-103">FIRSTORNULL ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="deb63-104">Funkce `FIRSTORNULL` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento záznam není prázdný.</span><span class="sxs-lookup"><span data-stu-id="deb63-104">The `FIRSTORNULL` function returns the first record of the specified list as a *Container (record)* value, if that record isn't empty.</span></span> <span data-ttu-id="deb63-105">Je-li záznam prázdný, vrátí tato funkce hodnotu typu *kontejner (záznam)* s hodnotou null.</span><span class="sxs-lookup"><span data-stu-id="deb63-105">If the record is empty, this function returns a null *Container (record)* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="deb63-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="deb63-106">Syntax</span></span>

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a><span data-ttu-id="deb63-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="deb63-107">Arguments</span></span>

<span data-ttu-id="deb63-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="deb63-108">`list`: *Record list*</span></span>

<span data-ttu-id="deb63-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="deb63-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="deb63-110">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="deb63-110">Return values</span></span>

<span data-ttu-id="deb63-111">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="deb63-111">*Container (record)*</span></span>

<span data-ttu-id="deb63-112">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="deb63-112">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="deb63-113">Příklad</span><span class="sxs-lookup"><span data-stu-id="deb63-113">Example</span></span>

<span data-ttu-id="deb63-114">Výraz `FIRSTORNULL(SPLIT("",1)).Value` vrátí prázdný řetězec (**""**).</span><span class="sxs-lookup"><span data-stu-id="deb63-114">The expression `FIRSTORNULL(SPLIT("",1)).Value` returns an empty string (**""**).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="deb63-115">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="deb63-115">Additional resources</span></span>

[<span data-ttu-id="deb63-116">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="deb63-116">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]