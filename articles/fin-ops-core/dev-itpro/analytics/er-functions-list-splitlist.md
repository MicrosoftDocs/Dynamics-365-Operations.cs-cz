---
title: Funkce elektronického výkaznictví SPLITLIST
description: Toto téma obsahuje obecné informace o použití funkce SPLITLIST elektronického výkaznictví.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745562"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="13406-103">Funkce elektronického výkaznictví SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="13406-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13406-104">Funkce `SPLITLIST` rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů.</span><span class="sxs-lookup"><span data-stu-id="13406-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="13406-105">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="13406-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="13406-106">Syntaxe 1</span><span class="sxs-lookup"><span data-stu-id="13406-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="13406-107">Syntaxe 2</span><span class="sxs-lookup"><span data-stu-id="13406-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="13406-108">Argumenty</span><span class="sxs-lookup"><span data-stu-id="13406-108">Arguments</span></span>

<span data-ttu-id="13406-109">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="13406-109">`list`: *Record list*</span></span>

<span data-ttu-id="13406-110">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="13406-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="13406-111">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="13406-111">`number`: *Integer*</span></span>

<span data-ttu-id="13406-112">Maximální počet zobrazených záznamů na dávku.</span><span class="sxs-lookup"><span data-stu-id="13406-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="13406-113">`on-demand reading flag`: *logická hodnota*</span><span class="sxs-lookup"><span data-stu-id="13406-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="13406-114">*Booleovská* hodnota určující, zda mají být prvky dílčích seznamů generovány na vyžádání.</span><span class="sxs-lookup"><span data-stu-id="13406-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="13406-115">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="13406-115">Return values</span></span>

<span data-ttu-id="13406-116">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="13406-116">*Record list*</span></span>

<span data-ttu-id="13406-117">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="13406-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="13406-118">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="13406-118">Usage notes</span></span>

<span data-ttu-id="13406-119">Vrácený seznam dávek obsahuje následující prvky:</span><span class="sxs-lookup"><span data-stu-id="13406-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="13406-120">**Value:** *seznam*</span><span class="sxs-lookup"><span data-stu-id="13406-120">**Value:** *List*</span></span>

    <span data-ttu-id="13406-121">Seznam záznamů, které patří do aktuální dávky.</span><span class="sxs-lookup"><span data-stu-id="13406-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="13406-122">**BatchNumber:** *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="13406-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="13406-123">Číslo aktuální dávky ve vráceném seznamu.</span><span class="sxs-lookup"><span data-stu-id="13406-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="13406-124">Když je příznak čtení na vyžádání nastaven na **Pravda**, dílčí seznamy jsou generovány na vyžádání, což umožňuje snížit spotřebu paměti, ale může dojít k pomalejšímu zpracování, pokud se prvky nepoužívají postupně.</span><span class="sxs-lookup"><span data-stu-id="13406-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="13406-125">Příklad</span><span class="sxs-lookup"><span data-stu-id="13406-125">Example</span></span>

<span data-ttu-id="13406-126">V následujícím příkladu je datový zdroj **Řádky** vytvořen jako seznam záznamů se třemi záznamy.</span><span class="sxs-lookup"><span data-stu-id="13406-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="13406-127">Tento seznam je rozdělen do dávek, z nichž každá obsahuje až dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="13406-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="13406-128">Následující obrázek znázorňuje navržené rozvržení formátu.</span><span class="sxs-lookup"><span data-stu-id="13406-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="13406-129">V tomto rozvržení formátu jsou vytvořeny vazby na datový zdroj **Řádky** za účelem vygenerování výstupu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="13406-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="13406-130">Tento výstup představuje jednotlivé uzly pro každou dávku a záznamy v ní.</span><span class="sxs-lookup"><span data-stu-id="13406-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="13406-131">Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</span><span class="sxs-lookup"><span data-stu-id="13406-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="13406-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="13406-132">Additional resources</span></span>

[<span data-ttu-id="13406-133">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="13406-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
