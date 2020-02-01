---
title: Funkce elektronického výkaznictví EMPTYRECORD
description: Toto téma obsahuje obecné informace o použití funkce EMPTYRECORD elektronického výkaznictví.
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916883"
---
# <span data-ttu-id="0aa3f-103"><a name="EMPTYRECORD">Funkce elektronického výkaznictví EMPTYRECORD</a></span><span class="sxs-lookup"><span data-stu-id="0aa3f-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aa3f-104">Funkce `EMPTYRECORD` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aa3f-105">Syntax</span></span>

```
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="0aa3f-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="0aa3f-106">Arguments</span></span>

<span data-ttu-id="0aa3f-107">`list`: *seznam záznamů* nebo *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="0aa3f-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="0aa3f-108">Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0aa3f-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="0aa3f-109">Return values</span></span>

<span data-ttu-id="0aa3f-110">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="0aa3f-110">*Container (record)*</span></span>

<span data-ttu-id="0aa3f-111">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0aa3f-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="0aa3f-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="0aa3f-113">Záznam null je záznam, kde všechna pole mají prázdnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="0aa3f-114">Prázdná hodnota je **0** (nula) pro čísla, prázdný řetězec pro řetězce atd.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="0aa3f-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="0aa3f-115">Example</span></span>

<span data-ttu-id="0aa3f-116">`EMPTYRECORD (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="0aa3f-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="0aa3f-117">Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="0aa3f-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0aa3f-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0aa3f-118">Additional resources</span></span>

[<span data-ttu-id="0aa3f-119">Funkce záznamu</span><span class="sxs-lookup"><span data-stu-id="0aa3f-119">Record functions</span></span>](er-functions-category-record.md)