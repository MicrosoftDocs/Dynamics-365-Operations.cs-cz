---
title: Funkce elektronického výkaznictví NULLCONTAINER
description: Toto téma obsahuje obecné informace o použití funkce NULLCONTAINER elektronického výkaznictví.
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
ms.openlocfilehash: 1dde102acf18e451cb895b51b28d22102f38936c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915779"
---
# <span data-ttu-id="f7990-103"><a name="NULLCONTAINER">Funkce elektronického výkaznictví NULLCONTAINER</a></span><span class="sxs-lookup"><span data-stu-id="f7990-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7990-104">Funkce `NULLCONTAINER` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.</span><span class="sxs-lookup"><span data-stu-id="f7990-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7990-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7990-105">Syntax</span></span>

```
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="f7990-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="f7990-106">Arguments</span></span>

<span data-ttu-id="f7990-107">`list`: *seznam záznamů* nebo *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="f7990-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="f7990-108">Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="f7990-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f7990-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="f7990-109">Return values</span></span>

<span data-ttu-id="f7990-110">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="f7990-110">*Container (record)*</span></span>

<span data-ttu-id="f7990-111">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="f7990-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f7990-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="f7990-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="f7990-113">Tato funkce je zastaralá.</span><span class="sxs-lookup"><span data-stu-id="f7990-113">This function is obsolete.</span></span> <span data-ttu-id="f7990-114">Místo toho použijte funkci `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="f7990-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="f7990-115">Další informace naleznete v tématu [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="f7990-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="f7990-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="f7990-116">Example</span></span>

<span data-ttu-id="f7990-117">`NULLCONTAINER (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="f7990-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="f7990-118">Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="f7990-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7990-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f7990-119">Additional resources</span></span>

[<span data-ttu-id="f7990-120">Funkce záznamu</span><span class="sxs-lookup"><span data-stu-id="f7990-120">Record functions</span></span>](er-functions-category-record.md)
