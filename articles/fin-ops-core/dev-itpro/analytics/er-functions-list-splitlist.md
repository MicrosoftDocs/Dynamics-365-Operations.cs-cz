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
ms.openlocfilehash: 950fc711f0e28eaee7fabc437ee16a022e1b705e
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744784"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="7f704-103">Funkce elektronického výkaznictví SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="7f704-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f704-104">Funkce `SPLITLIST` rozdělí zadaný seznam na podseznamy (neboli dávky), přičemž každá z nich obsahuje zadaný počet záznamů.</span><span class="sxs-lookup"><span data-stu-id="7f704-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="7f704-105">Funkce potom vrátí výsledek jako novou hodnotu typu *seznam záznamů*, která se skládá z dávek.</span><span class="sxs-lookup"><span data-stu-id="7f704-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f704-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f704-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="7f704-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="7f704-107">Arguments</span></span>

<span data-ttu-id="7f704-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="7f704-108">`list`: *Record list*</span></span>

<span data-ttu-id="7f704-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="7f704-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7f704-110">`number`: *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="7f704-110">`number`: *Integer*</span></span>

<span data-ttu-id="7f704-111">Maximální počet zobrazených záznamů na dávku.</span><span class="sxs-lookup"><span data-stu-id="7f704-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f704-112">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="7f704-112">Return values</span></span>

<span data-ttu-id="7f704-113">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="7f704-113">*Record list*</span></span>

<span data-ttu-id="7f704-114">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="7f704-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7f704-115">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="7f704-115">Usage notes</span></span>

<span data-ttu-id="7f704-116">Vrácený seznam dávek obsahuje následující prvky:</span><span class="sxs-lookup"><span data-stu-id="7f704-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="7f704-117">**Value:** *seznam*</span><span class="sxs-lookup"><span data-stu-id="7f704-117">**Value:** *List*</span></span>

    <span data-ttu-id="7f704-118">Seznam záznamů, které patří do aktuální dávky.</span><span class="sxs-lookup"><span data-stu-id="7f704-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="7f704-119">**BatchNumber:** *celé číslo*</span><span class="sxs-lookup"><span data-stu-id="7f704-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="7f704-120">Číslo aktuální dávky ve vráceném seznamu.</span><span class="sxs-lookup"><span data-stu-id="7f704-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="7f704-121">Příklad</span><span class="sxs-lookup"><span data-stu-id="7f704-121">Example</span></span>

<span data-ttu-id="7f704-122">V následujícím příkladu je datový zdroj **Řádky** vytvořen jako seznam záznamů se třemi záznamy.</span><span class="sxs-lookup"><span data-stu-id="7f704-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="7f704-123">Tento seznam je rozdělen do dávek, z nichž každá obsahuje až dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="7f704-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="7f704-124">Následující obrázek znázorňuje navržené rozvržení formátu.</span><span class="sxs-lookup"><span data-stu-id="7f704-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="7f704-125">V tomto rozvržení formátu jsou vytvořeny vazby na datový zdroj **Řádky** za účelem vygenerování výstupu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="7f704-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="7f704-126">Tento výstup představuje jednotlivé uzly pro každou dávku a záznamy v ní.</span><span class="sxs-lookup"><span data-stu-id="7f704-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="7f704-127">Následující obrázek znázorňuje výsledek při spuštění navrženého formátu.</span><span class="sxs-lookup"><span data-stu-id="7f704-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="7f704-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="7f704-128">Additional resources</span></span>

[<span data-ttu-id="7f704-129">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="7f704-129">List functions</span></span>](er-functions-category-list.md)
