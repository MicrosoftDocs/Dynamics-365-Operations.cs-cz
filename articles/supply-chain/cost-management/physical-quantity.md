---
title: "Hodnoty objektu zásob"
description: "Tento článek obsahuje informace o výpočtu hodnot objektu zásob."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4aec6e70325c7e4d00e6070293a1ab0c719e420b
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="inventory-object-values"></a><span data-ttu-id="2b95f-103">Hodnoty objektu zásob</span><span class="sxs-lookup"><span data-stu-id="2b95f-103">Inventory object values</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2b95f-104">Tento článek obsahuje informace o výpočtu hodnot objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="2b95f-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="2b95f-105">Nová funkce **„fyzické množství“** umožňuje zobrazit hodnoty určitého objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="2b95f-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="2b95f-106">Nákladový objekt představuje úroveň entity, kde bude probíhat účtování zásob.</span><span class="sxs-lookup"><span data-stu-id="2b95f-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="2b95f-107">Další informace o nákladových objektech naleznete v tématu [Nákladové objekty](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="2b95f-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="2b95f-108">Pokud chcete zobrazit hodnoty konkrétního objektu zásob, klikněte na tlačítko **Fyzické množství** na stránce **Objekt nákladů**.</span><span class="sxs-lookup"><span data-stu-id="2b95f-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="2b95f-109">Zde je způsob výpočtu hodnoty objektu zásob:</span><span class="sxs-lookup"><span data-stu-id="2b95f-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="2b95f-110">Objekt zásob.Hodnota = Objektu nákladů.Průměrné náklady na jednotku x Objekt zásob.Množství</span><span class="sxs-lookup"><span data-stu-id="2b95f-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="2b95f-111">Následující příklad ukazuje způsob výpočtu hodnot objektu zásob a objektu nákladů.</span><span class="sxs-lookup"><span data-stu-id="2b95f-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="2b95f-112">U položky A jsou registrovány dvě události příjemky produktu:</span><span class="sxs-lookup"><span data-stu-id="2b95f-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="2b95f-113">Příjemka produktu 1: Množství = 100 kusů., Množství = 1 000,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="2b95f-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="2b95f-114">= B1</span><span class="sxs-lookup"><span data-stu-id="2b95f-114">= B1</span></span>
-   <span data-ttu-id="2b95f-115">Příjemka produktu 2: Množství = 50 kusů., Množství = 800,00 Kč, Pracoviště = 1, Sklad = 11, Č. dávky</span><span class="sxs-lookup"><span data-stu-id="2b95f-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="2b95f-116">= B2</span><span class="sxs-lookup"><span data-stu-id="2b95f-116">= B2</span></span>

<span data-ttu-id="2b95f-117">Následující tabulka zobrazuje výsledek výpočtu nákladového objektu.</span><span class="sxs-lookup"><span data-stu-id="2b95f-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="2b95f-118">Výsledky lze zobrazit na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="2b95f-118">You can view the result on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="2b95f-119">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="2b95f-119">Object type</span></span></th>
<th><span data-ttu-id="2b95f-120">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="2b95f-120">Item number</span></span></th>
<th><span data-ttu-id="2b95f-121">Lokalita</span><span class="sxs-lookup"><span data-stu-id="2b95f-121">Site</span></span></th>
<th><span data-ttu-id="2b95f-122">Množství</span><span class="sxs-lookup"><span data-stu-id="2b95f-122">Quantity</span></span></th>
<th><span data-ttu-id="2b95f-123">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="2b95f-123">Inventory unit</span></span></th>
<th><span data-ttu-id="2b95f-124">Hodnota</span><span class="sxs-lookup"><span data-stu-id="2b95f-124">Value</span></span></th>
<th><span data-ttu-id="2b95f-125">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="2b95f-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b95f-126">Objekt nákladů</span><span class="sxs-lookup"><span data-stu-id="2b95f-126">Cost object</span></span></td>
<td><span data-ttu-id="2b95f-127">O</span><span class="sxs-lookup"><span data-stu-id="2b95f-127">A</span></span></td>
<td><span data-ttu-id="2b95f-128">1</span><span class="sxs-lookup"><span data-stu-id="2b95f-128">1</span></span></td>
<td><span data-ttu-id="2b95f-129">150</span><span class="sxs-lookup"><span data-stu-id="2b95f-129">150</span></span></td>
<td><span data-ttu-id="2b95f-130">Ks</span><span class="sxs-lookup"><span data-stu-id="2b95f-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="2b95f-131">1 800,00 Kč</span><span class="sxs-lookup"><span data-stu-id="2b95f-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="2b95f-132">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="2b95f-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="2b95f-133">Následující tabulka zobrazuje výsledek výpočtu objektu zásob.</span><span class="sxs-lookup"><span data-stu-id="2b95f-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="2b95f-134">Výsledky lze zobrazit kliknutím na možnost **Fyzické množství** na stránce **Nákladový objekt**.</span><span class="sxs-lookup"><span data-stu-id="2b95f-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

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
<th><span data-ttu-id="2b95f-135">Typ objektu</span><span class="sxs-lookup"><span data-stu-id="2b95f-135">Object type</span></span></th>
<th><span data-ttu-id="2b95f-136">Číslo zboží</span><span class="sxs-lookup"><span data-stu-id="2b95f-136">Item number</span></span></th>
<th><span data-ttu-id="2b95f-137">Lokalita</span><span class="sxs-lookup"><span data-stu-id="2b95f-137">Site</span></span></th>
<th><span data-ttu-id="2b95f-138">Sklad</span><span class="sxs-lookup"><span data-stu-id="2b95f-138">Warehouse</span></span></th>
<th><span data-ttu-id="2b95f-139">Č. dávky</span><span class="sxs-lookup"><span data-stu-id="2b95f-139">Batch No.</span></span></th>
<th><span data-ttu-id="2b95f-140">Množství</span><span class="sxs-lookup"><span data-stu-id="2b95f-140">Quantity</span></span></th>
<th><span data-ttu-id="2b95f-141">Skladová jednotka</span><span class="sxs-lookup"><span data-stu-id="2b95f-141">Inventory unit</span></span></th>
<th><span data-ttu-id="2b95f-142">Hodnota</span><span class="sxs-lookup"><span data-stu-id="2b95f-142">Value</span></span></th>
<th><span data-ttu-id="2b95f-143">Průměrné náklady na jednotku</span><span class="sxs-lookup"><span data-stu-id="2b95f-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2b95f-144">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="2b95f-144">Inventory object</span></span></td>
<td><span data-ttu-id="2b95f-145">O</span><span class="sxs-lookup"><span data-stu-id="2b95f-145">A</span></span></td>
<td><span data-ttu-id="2b95f-146">1</span><span class="sxs-lookup"><span data-stu-id="2b95f-146">1</span></span></td>
<td><span data-ttu-id="2b95f-147">11</span><span class="sxs-lookup"><span data-stu-id="2b95f-147">11</span></span></td>
<td><span data-ttu-id="2b95f-148">B1</span><span class="sxs-lookup"><span data-stu-id="2b95f-148">B1</span></span></td>
<td><span data-ttu-id="2b95f-149">100</span><span class="sxs-lookup"><span data-stu-id="2b95f-149">100</span></span></td>
<td><span data-ttu-id="2b95f-150">Ks</span><span class="sxs-lookup"><span data-stu-id="2b95f-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="2b95f-151">1 200,00 Kč.</span><span class="sxs-lookup"><span data-stu-id="2b95f-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="2b95f-152">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="2b95f-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2b95f-153">Objekt zásob</span><span class="sxs-lookup"><span data-stu-id="2b95f-153">Inventory object</span></span></td>
<td><span data-ttu-id="2b95f-154">A.</span><span class="sxs-lookup"><span data-stu-id="2b95f-154">A</span></span></td>
<td><span data-ttu-id="2b95f-155">1</span><span class="sxs-lookup"><span data-stu-id="2b95f-155">1</span></span></td>
<td><span data-ttu-id="2b95f-156">11</span><span class="sxs-lookup"><span data-stu-id="2b95f-156">11</span></span></td>
<td><span data-ttu-id="2b95f-157">B2</span><span class="sxs-lookup"><span data-stu-id="2b95f-157">B2</span></span></td>
<td><span data-ttu-id="2b95f-158">50</span><span class="sxs-lookup"><span data-stu-id="2b95f-158">50</span></span></td>
<td><span data-ttu-id="2b95f-159">Ks</span><span class="sxs-lookup"><span data-stu-id="2b95f-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="2b95f-160">600,00 Kč</span><span class="sxs-lookup"><span data-stu-id="2b95f-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="2b95f-161">12,00 Kč</span><span class="sxs-lookup"><span data-stu-id="2b95f-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="2b95f-162">Viz také</span><span class="sxs-lookup"><span data-stu-id="2b95f-162">See also</span></span>
--------

[<span data-ttu-id="2b95f-163">Nákladové objekty</span><span class="sxs-lookup"><span data-stu-id="2b95f-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="2b95f-164">Položky nákladů</span><span class="sxs-lookup"><span data-stu-id="2b95f-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="2b95f-165">Co je nového a co se změnilo</span><span class="sxs-lookup"><span data-stu-id="2b95f-165">What's new and changed</span></span>](/dynamics365/unified-operations/dev-itpro/get-started/whats-new-changed)




