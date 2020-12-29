---
title: Hodnoty objektu zásob
description: Tento článek obsahuje informace o výpočtu hodnot objektu zásob.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daa36dad4009cc25b89363dcff6b4496205522e3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423699"
---
# <a name="inventory-object-values"></a><span data-ttu-id="23981-103">Hodnoty objektu zásob</span><span class="sxs-lookup"><span data-stu-id="23981-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23981-104">Tento článek obsahuje informace o výpočtu hodnot objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="23981-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="23981-105">Nová funkce **„fyzické množství“** umožňuje zobrazit hodnoty určitého objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="23981-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="23981-106">Nákladový objekt představuje úroveň entity, kde bude probíhat účtování zásob.</span><span class="sxs-lookup"><span data-stu-id="23981-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="23981-107">Další informace o nákladových objektech naleznete v tématu [Nákladové objekty](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="23981-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="23981-108">Pokud chcete zobrazit hodnoty konkrétního objektu zásob, klikněte na tlačítko **Fyzické množství** na stránce **Objekt nákladů**.</span><span class="sxs-lookup"><span data-stu-id="23981-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="23981-109">Zde je způsob výpočtu hodnoty objektu zásob:</span><span class="sxs-lookup"><span data-stu-id="23981-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="23981-110">Objekt zásob.Hodnota = Objektu nákladů.Průměrné náklady na jednotku x Objekt zásob.Množství</span><span class="sxs-lookup"><span data-stu-id="23981-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="23981-111">Následující příklad ukazuje způsob výpočtu hodnot objektu zásob a objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="23981-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="23981-112">U položky A jsou registrovány dvě události příjemky produktu:</span><span class="sxs-lookup"><span data-stu-id="23981-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="23981-113">Příjemka produktu 1: Množství = 100 kusů., Množství = 1 000,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="23981-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="23981-114">= B1</span><span class="sxs-lookup"><span data-stu-id="23981-114">= B1</span></span>
-   <span data-ttu-id="23981-115">Příjemka produktu 2: Množství = 50 kusů., Množství = 800,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="23981-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="23981-116">= B2</span><span class="sxs-lookup"><span data-stu-id="23981-116">= B2</span></span>

<span data-ttu-id="23981-117">Následující tabulka zobrazuje výsledek výpočtu nákladového objektu.</span><span class="sxs-lookup"><span data-stu-id="23981-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="23981-118">Výsledky lze zobrazit na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="23981-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="23981-119">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="23981-119">Object type</span></span></th>
<th><span data-ttu-id="23981-120">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="23981-120">Item number</span></span></th>
<th><span data-ttu-id="23981-121">Lokalita</span><span class="sxs-lookup"><span data-stu-id="23981-121">Site</span></span></th>
<th><span data-ttu-id="23981-122">Množství</span><span class="sxs-lookup"><span data-stu-id="23981-122">Quantity</span></span></th>
<th><span data-ttu-id="23981-123">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="23981-123">Inventory unit</span></span></th>
<th><span data-ttu-id="23981-124">Hodnota</span><span class="sxs-lookup"><span data-stu-id="23981-124">Value</span></span></th>
<th><span data-ttu-id="23981-125">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="23981-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23981-126">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="23981-126">Cost object</span></span></td>
<td><span data-ttu-id="23981-127">O</span><span class="sxs-lookup"><span data-stu-id="23981-127">A</span></span></td>
<td><span data-ttu-id="23981-128">1</span><span class="sxs-lookup"><span data-stu-id="23981-128">1</span></span></td>
<td><span data-ttu-id="23981-129">150</span><span class="sxs-lookup"><span data-stu-id="23981-129">150</span></span></td>
<td><span data-ttu-id="23981-130">Ks</span><span class="sxs-lookup"><span data-stu-id="23981-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="23981-131">1 800,00 Kč</span><span class="sxs-lookup"><span data-stu-id="23981-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="23981-132">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="23981-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="23981-133">Následující tabulka zobrazuje výsledek výpočtu objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="23981-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="23981-134">Výsledky lze zobrazit kliknutím na možnost **Fyzické množství** na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="23981-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="23981-135">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="23981-135">Object type</span></span></th>
<th><span data-ttu-id="23981-136">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="23981-136">Item number</span></span></th>
<th><span data-ttu-id="23981-137">Lokalita</span><span class="sxs-lookup"><span data-stu-id="23981-137">Site</span></span></th>
<th><span data-ttu-id="23981-138">Sklad</span><span class="sxs-lookup"><span data-stu-id="23981-138">Warehouse</span></span></th>
<th><span data-ttu-id="23981-139">Č. dávky</span><span class="sxs-lookup"><span data-stu-id="23981-139">Batch No.</span></span></th>
<th><span data-ttu-id="23981-140">Množství</span><span class="sxs-lookup"><span data-stu-id="23981-140">Quantity</span></span></th>
<th><span data-ttu-id="23981-141">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="23981-141">Inventory unit</span></span></th>
<th><span data-ttu-id="23981-142">Hodnota</span><span class="sxs-lookup"><span data-stu-id="23981-142">Value</span></span></th>
<th><span data-ttu-id="23981-143">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="23981-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23981-144">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="23981-144">Inventory object</span></span></td>
<td><span data-ttu-id="23981-145">O</span><span class="sxs-lookup"><span data-stu-id="23981-145">A</span></span></td>
<td><span data-ttu-id="23981-146">1</span><span class="sxs-lookup"><span data-stu-id="23981-146">1</span></span></td>
<td><span data-ttu-id="23981-147">11</span><span class="sxs-lookup"><span data-stu-id="23981-147">11</span></span></td>
<td><span data-ttu-id="23981-148">B1</span><span class="sxs-lookup"><span data-stu-id="23981-148">B1</span></span></td>
<td><span data-ttu-id="23981-149">100</span><span class="sxs-lookup"><span data-stu-id="23981-149">100</span></span></td>
<td><span data-ttu-id="23981-150">Ks</span><span class="sxs-lookup"><span data-stu-id="23981-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="23981-151">1 200,00 Kč.</span><span class="sxs-lookup"><span data-stu-id="23981-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="23981-152">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="23981-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="23981-153">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="23981-153">Inventory object</span></span></td>
<td><span data-ttu-id="23981-154">A</span><span class="sxs-lookup"><span data-stu-id="23981-154">A</span></span></td>
<td><span data-ttu-id="23981-155">1</span><span class="sxs-lookup"><span data-stu-id="23981-155">1</span></span></td>
<td><span data-ttu-id="23981-156">11</span><span class="sxs-lookup"><span data-stu-id="23981-156">11</span></span></td>
<td><span data-ttu-id="23981-157">B2</span><span class="sxs-lookup"><span data-stu-id="23981-157">B2</span></span></td>
<td><span data-ttu-id="23981-158">50</span><span class="sxs-lookup"><span data-stu-id="23981-158">50</span></span></td>
<td><span data-ttu-id="23981-159">Ks</span><span class="sxs-lookup"><span data-stu-id="23981-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="23981-160">600,00 Kč</span><span class="sxs-lookup"><span data-stu-id="23981-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="23981-161">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="23981-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="23981-162">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="23981-162">Additional resources</span></span>
--------

[<span data-ttu-id="23981-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="23981-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="23981-164">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="23981-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="23981-165">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="23981-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



