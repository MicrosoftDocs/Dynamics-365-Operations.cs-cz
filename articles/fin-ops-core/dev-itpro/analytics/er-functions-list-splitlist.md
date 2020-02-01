---
title: Funkce elektronického výkaznictví SPLITLIST
description: Toto téma obsahuje obecné informace o použití funkce SPLITLIST elektronického výkaznictví.
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
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917205"
---
# <span data-ttu-id="7e2e6-103"><a name="SPLITLIST">Funkce elektronického výkaznictví SPLITLIST</a></span><span class="sxs-lookup"><span data-stu-id="7e2e6-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e2e6-104">Funkce `SPLITLIST` rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="7e2e6-105">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e2e6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e2e6-106">Syntax</span></span>

```
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="7e2e6-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="7e2e6-107">Arguments</span></span>

<span data-ttu-id="7e2e6-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="7e2e6-108">`list`: *Record list*</span></span>

<span data-ttu-id="7e2e6-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7e2e6-110">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="7e2e6-110">`number`: *Integer*</span></span>

<span data-ttu-id="7e2e6-111">Maximální počet zobrazených záznamů na dávku.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e2e6-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7e2e6-112">Return values</span></span>

<span data-ttu-id="7e2e6-113">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="7e2e6-113">*Record list*</span></span>

<span data-ttu-id="7e2e6-114">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7e2e6-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="7e2e6-115">Usage notes</span></span>

<span data-ttu-id="7e2e6-116">Vrácený seznam dávek obsahuje následující prvky:</span><span class="sxs-lookup"><span data-stu-id="7e2e6-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="7e2e6-117">**Value:** *seznam*</span><span class="sxs-lookup"><span data-stu-id="7e2e6-117">**Value:** *List*</span></span>

    <span data-ttu-id="7e2e6-118">Seznam záznamů, které patří do aktuální dávky.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="7e2e6-119">**BatchNumber:** *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="7e2e6-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="7e2e6-120">Číslo aktuální dávky ve vráceném seznamu.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="7e2e6-121">Příklad</span><span class="sxs-lookup"><span data-stu-id="7e2e6-121">Example</span></span>

<span data-ttu-id="7e2e6-122">V následujícím příkladu je datový zdroj **Řádky** vytvořen jako seznam záznamů se třemi záznamy.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="7e2e6-123">Tento seznam je rozdělen do dávek, z nichž každá obsahuje až dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="7e2e6-124">Následující obrázek znázorňuje navržené rozvržení formátu.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="7e2e6-125">V tomto rozvržení formátu jsou vytvořeny vazby na datový zdroj **Řádky** za účelem vygenerování výstupu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="7e2e6-126">Tento výstup představuje jednotlivé uzly pro každou dávku a záznamy v ní.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="7e2e6-127">Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</span><span class="sxs-lookup"><span data-stu-id="7e2e6-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="7e2e6-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7e2e6-128">Additional resources</span></span>

[<span data-ttu-id="7e2e6-129">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="7e2e6-129">List functions</span></span>](er-functions-category-list.md)