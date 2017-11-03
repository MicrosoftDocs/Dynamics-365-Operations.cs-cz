---
title: "Zadání kombinací účtu a dimenze (řízení segmentového zadání)"
description: "Tento článek popisuje způsob zadání kombinací účtu a dimenzí nebo účtů hlavní knihy. Zadávání je obvykle označováno jako řízení segmentovaného zadávání."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a4d8be319d74610bb2c1d4532a6d204d092bce84
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="b5324-104">Zadání kombinací účtu a dimenze (řízení segmentového zadání)</span><span class="sxs-lookup"><span data-stu-id="b5324-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b5324-105">Tento článek popisuje způsob zadání kombinací účtu a dimenzí nebo účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b5324-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="b5324-106">Zadávání je obvykle označováno jako řízení segmentovaného zadávání.</span><span class="sxs-lookup"><span data-stu-id="b5324-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="b5324-107">Uživatelé zadávají kombinace účtů a dimenzí na různých stránkách, například na stránkách pro hlavní deníky, rozpočtování a definice účtování.</span><span class="sxs-lookup"><span data-stu-id="b5324-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="b5324-108">Platné kombinace účtu a dimenzí závisí na účetních strukturách přiřazených k hlavní knize a rozšířených pravidlech přiřazených účetním strukturám.</span><span class="sxs-lookup"><span data-stu-id="b5324-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="b5324-109">Když uživatelé zadávají kombinaci, mohou hodnoty zadat buď ručně, nebo využít rozsáhlou funkcionalitu vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b5324-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="b5324-110">Pokud zadáte pole, můžete začít psát a bude vyhledána hodnota a popis.</span><span class="sxs-lookup"><span data-stu-id="b5324-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="b5324-111">Například pokud zadáte 180, bude se hledat libovolná hodnot, která začíná touto číselnou kombinaci.</span><span class="sxs-lookup"><span data-stu-id="b5324-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="b5324-112">Nebo můžete zadat hotovost a vyhledají se libovolné hodnoty, které má popis začínající slovem Hotovost.</span><span class="sxs-lookup"><span data-stu-id="b5324-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="b5324-113">K hledání můžete také použít zástupné znaky, jako \*Hotovost nebo \*180, pokud hodnota nebo popis obsahuje vyhledávací kritéria.</span><span class="sxs-lookup"><span data-stu-id="b5324-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="b5324-114">V následující tabulce jsou popsány klávesové zkratky, které lze použít, když je vyhledávání zavřené.</span><span class="sxs-lookup"><span data-stu-id="b5324-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5324-115">Klávesová zkratka</span><span class="sxs-lookup"><span data-stu-id="b5324-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="b5324-116">Akce</span><span class="sxs-lookup"><span data-stu-id="b5324-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5324-117">Alt + šipka dolů</span><span class="sxs-lookup"><span data-stu-id="b5324-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="b5324-118">Otevře vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b5324-118">Open the lookup.</span></span> <span data-ttu-id="b5324-119">Pokud stisknete klávesy Alt + šipka dolů ještě jednou, výběr se přesune do segmentů v plovoucím panelu.</span><span class="sxs-lookup"><span data-stu-id="b5324-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b5324-120">Enter a Shift + Enter</span><span class="sxs-lookup"><span data-stu-id="b5324-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="b5324-121">Oddělovač účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="b5324-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="b5324-122">Šipka doprava a šipka doleva</span><span class="sxs-lookup"><span data-stu-id="b5324-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="b5324-123">Přejde na následující nebo předchozí segment.</span><span class="sxs-lookup"><span data-stu-id="b5324-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5324-124">Karta</span><span class="sxs-lookup"><span data-stu-id="b5324-124">Tab</span></span></td>
<td><span data-ttu-id="b5324-125">Přejde k následujícímu poli v mřížce.</span><span class="sxs-lookup"><span data-stu-id="b5324-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b5324-126">V následující tabulce jsou popsány klávesové zkratky, které lze použít, když je vyhledávání otevřené.</span><span class="sxs-lookup"><span data-stu-id="b5324-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5324-127">Klávesová zkratka</span><span class="sxs-lookup"><span data-stu-id="b5324-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="b5324-128">Akce</span><span class="sxs-lookup"><span data-stu-id="b5324-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5324-129">Esc</span><span class="sxs-lookup"><span data-stu-id="b5324-129">Esc</span></span></td>
<td><span data-ttu-id="b5324-130">Zavření vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b5324-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="b5324-131">Šipka nahoru a šipka dolů</span><span class="sxs-lookup"><span data-stu-id="b5324-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="b5324-132">Page Up a Page Down</span><span class="sxs-lookup"><span data-stu-id="b5324-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="b5324-133">Home a End</span><span class="sxs-lookup"><span data-stu-id="b5324-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="b5324-134">Přejde na předchozí nebo následující hodnotu v seznamech, předchozí nebo následující skupinu hodnot anebo na první nebo poslední prvek ve vyhledání.</span><span class="sxs-lookup"><span data-stu-id="b5324-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b5324-135">Oddělovač účtové osnovy</span><span class="sxs-lookup"><span data-stu-id="b5324-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="b5324-136">Šipka doprava a šipka doleva</span><span class="sxs-lookup"><span data-stu-id="b5324-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="b5324-137">Přejde na následující nebo předchozí segment.</span><span class="sxs-lookup"><span data-stu-id="b5324-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5324-138">Karta</span><span class="sxs-lookup"><span data-stu-id="b5324-138">Tab</span></span></td>
<td><span data-ttu-id="b5324-139">Přejde k následujícímu poli v mřížce.</span><span class="sxs-lookup"><span data-stu-id="b5324-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b5324-140">Alt + W</span><span class="sxs-lookup"><span data-stu-id="b5324-140">Alt+W</span></span></td>
<td><span data-ttu-id="b5324-141">Přepne mezi režimy <strong>Zobrazit vše</strong> a <strong>Zobrazit platné</strong>.</span><span class="sxs-lookup"><span data-stu-id="b5324-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>

 




