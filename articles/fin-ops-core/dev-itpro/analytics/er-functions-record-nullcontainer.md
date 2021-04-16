---
title: Funkce elektronického výkaznictví NULLCONTAINER
description: Toto téma obsahuje obecné informace o použití funkce NULLCONTAINER elektronického výkaznictví.
author: NickSelin
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
ms.openlocfilehash: af6651ef3c62bd8d1285fa8179ac923d3c333ce7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746500"
---
# <a name="nullcontainer-er-function"></a><span data-ttu-id="ae970-103">Funkce elektronického výkaznictví NULLCONTAINER</span><span class="sxs-lookup"><span data-stu-id="ae970-103">NULLCONTAINER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae970-104">Funkce `NULLCONTAINER` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.</span><span class="sxs-lookup"><span data-stu-id="ae970-104">The `NULLCONTAINER` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae970-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae970-105">Syntax</span></span>

```vb
NULLCONTAINER (list)
```

## <a name="arguments"></a><span data-ttu-id="ae970-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="ae970-106">Arguments</span></span>

<span data-ttu-id="ae970-107">`list`: *seznam záznamů* nebo *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="ae970-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="ae970-108">Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="ae970-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="ae970-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="ae970-109">Return values</span></span>

<span data-ttu-id="ae970-110">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="ae970-110">*Container (record)*</span></span>

<span data-ttu-id="ae970-111">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="ae970-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ae970-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="ae970-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="ae970-113">Tato funkce je zastaralá.</span><span class="sxs-lookup"><span data-stu-id="ae970-113">This function is obsolete.</span></span> <span data-ttu-id="ae970-114">Místo toho použijte funkci `EMPTYRECORD`.</span><span class="sxs-lookup"><span data-stu-id="ae970-114">Use the `EMPTYRECORD` function instead.</span></span> <span data-ttu-id="ae970-115">Další informace naleznete v tématu [EMPTYRECORD](er-functions-record-emptyrecord.md).</span><span class="sxs-lookup"><span data-stu-id="ae970-115">For more information, see [EMPTYRECORD](er-functions-record-emptyrecord.md).</span></span>

## <a name="example"></a><span data-ttu-id="ae970-116">Příklad</span><span class="sxs-lookup"><span data-stu-id="ae970-116">Example</span></span>

<span data-ttu-id="ae970-117">`NULLCONTAINER (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="ae970-117">`NULLCONTAINER (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="ae970-118">Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="ae970-118">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae970-119">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ae970-119">Additional resources</span></span>

[<span data-ttu-id="ae970-120">Funkce záznamu</span><span class="sxs-lookup"><span data-stu-id="ae970-120">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]