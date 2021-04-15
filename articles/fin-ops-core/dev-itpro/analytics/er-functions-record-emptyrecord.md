---
title: Funkce elektronického výkaznictví EMPTYRECORD
description: Toto téma obsahuje obecné informace o použití funkce EMPTYRECORD elektronického výkaznictví.
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
ms.openlocfilehash: e614c06b4cfad628bbd8a966719ed994ce05b792
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746524"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="11270-103">Funkce elektronického výkaznictví EMPTYRECORD</span><span class="sxs-lookup"><span data-stu-id="11270-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11270-104">Funkce `EMPTYRECORD` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.</span><span class="sxs-lookup"><span data-stu-id="11270-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="11270-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11270-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="11270-106">Argumenty</span><span class="sxs-lookup"><span data-stu-id="11270-106">Arguments</span></span>

<span data-ttu-id="11270-107">`list`: *seznam záznamů* nebo *kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="11270-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="11270-108">Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.</span><span class="sxs-lookup"><span data-stu-id="11270-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="11270-109">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="11270-109">Return values</span></span>

<span data-ttu-id="11270-110">*Kontejner (záznam)*</span><span class="sxs-lookup"><span data-stu-id="11270-110">*Container (record)*</span></span>

<span data-ttu-id="11270-111">Výsledná hodnota atributu.</span><span class="sxs-lookup"><span data-stu-id="11270-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="11270-112">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="11270-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="11270-113">Záznam null je záznam, kde všechna pole mají prázdnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="11270-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="11270-114">Prázdná hodnota je **0** (nula) pro čísla, prázdný řetězec pro řetězce atd.</span><span class="sxs-lookup"><span data-stu-id="11270-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="11270-115">Příklad</span><span class="sxs-lookup"><span data-stu-id="11270-115">Example</span></span>

<span data-ttu-id="11270-116">`EMPTYRECORD (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="11270-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="11270-117">Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)</span><span class="sxs-lookup"><span data-stu-id="11270-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11270-118">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="11270-118">Additional resources</span></span>

[<span data-ttu-id="11270-119">Funkce záznamu</span><span class="sxs-lookup"><span data-stu-id="11270-119">Record functions</span></span>](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]