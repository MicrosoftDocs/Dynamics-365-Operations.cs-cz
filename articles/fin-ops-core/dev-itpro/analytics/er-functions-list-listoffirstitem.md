---
title: Funkce elektronického výkaznictví LISTOFFIRSTITEM
description: Toto téma obsahuje obecné informace o použití funkce LISTOFFIRSTITEM elektronického výkaznictví.
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917251"
---
# <span data-ttu-id="d5020-103"><a name="LISTOFFIRSTITEM">Funkce elektronického výkaznictví LISTOFFIRSTITEM</a></span><span class="sxs-lookup"><span data-stu-id="d5020-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5020-104">Funkce `LISTOFFIRSTITEM` vrátí hodnotu typu *seznam záznamů*, která obsahuje pouze první záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="d5020-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5020-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5020-105">Syntax</span></span>

```
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="d5020-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="d5020-106">Arguments</span></span>

<span data-ttu-id="d5020-107">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="d5020-107">`list`: *Record list*</span></span>

<span data-ttu-id="d5020-108">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="d5020-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d5020-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="d5020-109">Return values</span></span>

<span data-ttu-id="d5020-110">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="d5020-110">*Record list*</span></span>

<span data-ttu-id="d5020-111">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="d5020-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="d5020-112">Příklad</span><span class="sxs-lookup"><span data-stu-id="d5020-112">Example</span></span>

<span data-ttu-id="d5020-113">Výraz `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` vrátí textovou hodnotu **"A"**.</span><span class="sxs-lookup"><span data-stu-id="d5020-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d5020-114">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d5020-114">Additional resources</span></span>

[<span data-ttu-id="d5020-115">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="d5020-115">List functions</span></span>](er-functions-category-list.md)
