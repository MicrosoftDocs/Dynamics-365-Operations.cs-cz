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
ms.openlocfilehash: ea71bfc4b30164fd32e804bf83a46c49cd18d155
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041462"
---
# <span data-ttu-id="e8d39-103"><a name="NULLCONTAINER">Funkce elektronického výkaznictví NULLCONTAINER</a></span><span class="sxs-lookup"><span data-stu-id="e8d39-103"><a name="NULLCONTAINER">NULLCONTAINER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8d39-104">Funkce `NULLCONTAINER` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.</span><span class="sxs-lookup"><span data-stu-id="e8d39-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8d39-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8d39-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="e8d39-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="e8d39-106">Arguments</span></span>

<span data-ttu-id="e8d39-107">`list`: *seznam záznamů* nebo *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="e8d39-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="e8d39-108">Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="e8d39-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e8d39-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="e8d39-109">Return values</span></span>

<span data-ttu-id="e8d39-110">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="e8d39-110">*Container (record)*</span></span>

<span data-ttu-id="e8d39-111">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="e8d39-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e8d39-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="e8d39-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e8d39-113">Tato funkce je zastaralá.</span><span class="sxs-lookup"><span data-stu-id="e8d39-113">This function is obsolete.</span></span> <span data-ttu-id="e8d39-114">Místo toho použijte funkci `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="e8d39-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="e8d39-115">Další informace naleznete v tématu [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="e8d39-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="e8d39-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="e8d39-116">Example</span></span>

<span data-ttu-id="e8d39-117">`NULLCONTAINER (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="e8d39-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="e8d39-118">Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="e8d39-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8d39-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e8d39-119">Additional resources</span></span>

[<span data-ttu-id="e8d39-120">Funkce záznamu</span><span class="sxs-lookup"><span data-stu-id="e8d39-120">Record functions</span></span>](er-functions-category-record.md)
