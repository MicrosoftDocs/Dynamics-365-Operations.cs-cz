---
title: Hodnoty objektu zásob
description: Tento článek obsahuje informace o výpočtu hodnot objektu zásob.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e92c7889b11208c4d2b48eb279a104a7c226f904
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547852"
---
# <a name="inventory-object-values"></a><span data-ttu-id="09934-103">Hodnoty objektu zásob</span><span class="sxs-lookup"><span data-stu-id="09934-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09934-104">Tento článek obsahuje informace o výpočtu hodnot objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="09934-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="09934-105">Nová funkce **„fyzické množství“** umožňuje zobrazit hodnoty určitého objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="09934-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="09934-106">Nákladový objekt představuje úroveň entity, kde bude probíhat účtování zásob.</span><span class="sxs-lookup"><span data-stu-id="09934-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="09934-107">Další informace o nákladových objektech naleznete v tématu [Nákladové objekty](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="09934-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="09934-108">Pokud chcete zobrazit hodnoty konkrétního objektu zásob, klikněte na tlačítko **Fyzické množství** na stránce **Objekt nákladů**.</span><span class="sxs-lookup"><span data-stu-id="09934-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="09934-109">Zde je způsob výpočtu hodnoty objektu zásob:</span><span class="sxs-lookup"><span data-stu-id="09934-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="09934-110">Objekt zásob.Hodnota = Objektu nákladů.Průměrné náklady na jednotku x Objekt zásob.Množství</span><span class="sxs-lookup"><span data-stu-id="09934-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="09934-111">Následující příklad ukazuje způsob výpočtu hodnot objektu zásob a objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="09934-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="09934-112">U položky A jsou registrovány dvě události příjemky produktu:</span><span class="sxs-lookup"><span data-stu-id="09934-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="09934-113">Příjemka produktu 1: Množství = 100 kusů., Množství = 1 000,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="09934-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="09934-114">= B1</span><span class="sxs-lookup"><span data-stu-id="09934-114">= B1</span></span>
-   <span data-ttu-id="09934-115">Příjemka produktu 2: Množství = 50 kusů., Množství = 800,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="09934-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="09934-116">= B2</span><span class="sxs-lookup"><span data-stu-id="09934-116">= B2</span></span>

<span data-ttu-id="09934-117">Následující tabulka zobrazuje výsledek výpočtu nákladového objektu.</span><span class="sxs-lookup"><span data-stu-id="09934-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="09934-118">Výsledky lze zobrazit na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="09934-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09934-119">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="09934-119">Object type</span></span></th>
<th><span data-ttu-id="09934-120">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="09934-120">Item number</span></span></th>
<th><span data-ttu-id="09934-121">Lokalita</span><span class="sxs-lookup"><span data-stu-id="09934-121">Site</span></span></th>
<th><span data-ttu-id="09934-122">Množství</span><span class="sxs-lookup"><span data-stu-id="09934-122">Quantity</span></span></th>
<th><span data-ttu-id="09934-123">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="09934-123">Inventory unit</span></span></th>
<th><span data-ttu-id="09934-124">Hodnota</span><span class="sxs-lookup"><span data-stu-id="09934-124">Value</span></span></th>
<th><span data-ttu-id="09934-125">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="09934-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09934-126">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="09934-126">Cost object</span></span></td>
<td><span data-ttu-id="09934-127">O</span><span class="sxs-lookup"><span data-stu-id="09934-127">A</span></span></td>
<td><span data-ttu-id="09934-128">1</span><span class="sxs-lookup"><span data-stu-id="09934-128">1</span></span></td>
<td><span data-ttu-id="09934-129">150</span><span class="sxs-lookup"><span data-stu-id="09934-129">150</span></span></td>
<td><span data-ttu-id="09934-130">Ks</span><span class="sxs-lookup"><span data-stu-id="09934-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="09934-131">1 800,00 Kč</span><span class="sxs-lookup"><span data-stu-id="09934-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="09934-132">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="09934-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="09934-133">Následující tabulka zobrazuje výsledek výpočtu objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="09934-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="09934-134">Výsledky lze zobrazit kliknutím na možnost **Fyzické množství** na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="09934-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09934-135">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="09934-135">Object type</span></span></th>
<th><span data-ttu-id="09934-136">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="09934-136">Item number</span></span></th>
<th><span data-ttu-id="09934-137">Lokalita</span><span class="sxs-lookup"><span data-stu-id="09934-137">Site</span></span></th>
<th><span data-ttu-id="09934-138">Sklad</span><span class="sxs-lookup"><span data-stu-id="09934-138">Warehouse</span></span></th>
<th><span data-ttu-id="09934-139">Č. dávky</span><span class="sxs-lookup"><span data-stu-id="09934-139">Batch No.</span></span></th>
<th><span data-ttu-id="09934-140">Množství</span><span class="sxs-lookup"><span data-stu-id="09934-140">Quantity</span></span></th>
<th><span data-ttu-id="09934-141">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="09934-141">Inventory unit</span></span></th>
<th><span data-ttu-id="09934-142">Hodnota</span><span class="sxs-lookup"><span data-stu-id="09934-142">Value</span></span></th>
<th><span data-ttu-id="09934-143">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="09934-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09934-144">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="09934-144">Inventory object</span></span></td>
<td><span data-ttu-id="09934-145">O</span><span class="sxs-lookup"><span data-stu-id="09934-145">A</span></span></td>
<td><span data-ttu-id="09934-146">1</span><span class="sxs-lookup"><span data-stu-id="09934-146">1</span></span></td>
<td><span data-ttu-id="09934-147">11</span><span class="sxs-lookup"><span data-stu-id="09934-147">11</span></span></td>
<td><span data-ttu-id="09934-148">B1</span><span class="sxs-lookup"><span data-stu-id="09934-148">B1</span></span></td>
<td><span data-ttu-id="09934-149">100</span><span class="sxs-lookup"><span data-stu-id="09934-149">100</span></span></td>
<td><span data-ttu-id="09934-150">Ks</span><span class="sxs-lookup"><span data-stu-id="09934-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="09934-151">1 200,00 Kč.</span><span class="sxs-lookup"><span data-stu-id="09934-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="09934-152">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="09934-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09934-153">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="09934-153">Inventory object</span></span></td>
<td><span data-ttu-id="09934-154">A</span><span class="sxs-lookup"><span data-stu-id="09934-154">A</span></span></td>
<td><span data-ttu-id="09934-155">1</span><span class="sxs-lookup"><span data-stu-id="09934-155">1</span></span></td>
<td><span data-ttu-id="09934-156">11</span><span class="sxs-lookup"><span data-stu-id="09934-156">11</span></span></td>
<td><span data-ttu-id="09934-157">B2</span><span class="sxs-lookup"><span data-stu-id="09934-157">B2</span></span></td>
<td><span data-ttu-id="09934-158">50</span><span class="sxs-lookup"><span data-stu-id="09934-158">50</span></span></td>
<td><span data-ttu-id="09934-159">Ks</span><span class="sxs-lookup"><span data-stu-id="09934-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="09934-160">600,00 Kč</span><span class="sxs-lookup"><span data-stu-id="09934-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="09934-161">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="09934-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="09934-162">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="09934-162">Additional resources</span></span>
--------

[<span data-ttu-id="09934-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="09934-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="09934-164">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="09934-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="09934-165">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="09934-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



