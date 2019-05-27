---
title: Určení způsobu nakládání s vrácenými položkami
description: Určení způsobu nakládání s vrácenými položkami
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6fcdfec083aeb9c58d63f6e03542758e4d07e4d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560087"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="a37d8-103">Určení způsobu nakládání s vrácenými položkami</span><span class="sxs-lookup"><span data-stu-id="a37d8-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a37d8-104">Při zpracování vratky je třeba zadáním kódu důvodu vrácení identifikovat příčinu vrácení produktu.</span><span class="sxs-lookup"><span data-stu-id="a37d8-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="a37d8-105">Také je nutné zadáním dispozičního kódu a dispoziční akce určit, jak má být naloženo s vráceným produktem.</span><span class="sxs-lookup"><span data-stu-id="a37d8-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="a37d8-106">Dispoziční kód lze použít při vytvoření vratky, registraci doručené položky nebo aktualizaci dodacího listu pro položku a ukončení karanténního příkazu.</span><span class="sxs-lookup"><span data-stu-id="a37d8-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="a37d8-107">Můžete definovat libovolné dispoziční kódy, které si vyžaduje podpora obchodních procesů.</span><span class="sxs-lookup"><span data-stu-id="a37d8-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="a37d8-108">V následující tabulce je uvedena sada kódů, které jsou obvykle přidruženy k vyřazení vrácené položky.</span><span class="sxs-lookup"><span data-stu-id="a37d8-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a37d8-109">Typ dispozice</span><span class="sxs-lookup"><span data-stu-id="a37d8-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="a37d8-110">Běžný kód</span><span class="sxs-lookup"><span data-stu-id="a37d8-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="a37d8-111">popis</span><span class="sxs-lookup"><span data-stu-id="a37d8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-112">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="a37d8-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a37d8-113">SC</span><span class="sxs-lookup"><span data-stu-id="a37d8-113">SC</span></span></p></td>
<td><p><span data-ttu-id="a37d8-114">Likvidace nebo zničení</span><span class="sxs-lookup"><span data-stu-id="a37d8-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-115">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="a37d8-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a37d8-116">DC</span><span class="sxs-lookup"><span data-stu-id="a37d8-116">DC</span></span></p></td>
<td><p><span data-ttu-id="a37d8-117">Dar charitě</span><span class="sxs-lookup"><span data-stu-id="a37d8-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-118">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="a37d8-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a37d8-119">TD</span><span class="sxs-lookup"><span data-stu-id="a37d8-119">TD</span></span></p></td>
<td><p><span data-ttu-id="a37d8-120">Vyřazení třetí strany</span><span class="sxs-lookup"><span data-stu-id="a37d8-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-121">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="a37d8-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a37d8-122">SL</span><span class="sxs-lookup"><span data-stu-id="a37d8-122">SL</span></span></p></td>
<td><p><span data-ttu-id="a37d8-123">Konečný zůstatek</span><span class="sxs-lookup"><span data-stu-id="a37d8-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-124">Vyřazení</span><span class="sxs-lookup"><span data-stu-id="a37d8-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="a37d8-125">TS</span><span class="sxs-lookup"><span data-stu-id="a37d8-125">TS</span></span></p></td>
<td><p><span data-ttu-id="a37d8-126">Prodej třetí strany (sekundární trhy)</span><span class="sxs-lookup"><span data-stu-id="a37d8-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-127">Oprava nebo úprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a37d8-128">RW</span><span class="sxs-lookup"><span data-stu-id="a37d8-128">RW</span></span></p></td>
<td><p><span data-ttu-id="a37d8-129">Přepracování</span><span class="sxs-lookup"><span data-stu-id="a37d8-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-130">Oprava nebo úprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a37d8-131">RF</span><span class="sxs-lookup"><span data-stu-id="a37d8-131">RF</span></span></p></td>
<td><p><span data-ttu-id="a37d8-132">Přepracování</span><span class="sxs-lookup"><span data-stu-id="a37d8-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-133">Oprava nebo úprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a37d8-134">MD</span><span class="sxs-lookup"><span data-stu-id="a37d8-134">MD</span></span></p></td>
<td><p><span data-ttu-id="a37d8-135">Změna</span><span class="sxs-lookup"><span data-stu-id="a37d8-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-136">Oprava nebo úprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a37d8-137">RP</span><span class="sxs-lookup"><span data-stu-id="a37d8-137">RP</span></span></p></td>
<td><p><span data-ttu-id="a37d8-138">Oprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-139">Oprava nebo úprava</span><span class="sxs-lookup"><span data-stu-id="a37d8-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="a37d8-140">RV</span><span class="sxs-lookup"><span data-stu-id="a37d8-140">RV</span></span></p></td>
<td><p><span data-ttu-id="a37d8-141">Návrat dodavateli</span><span class="sxs-lookup"><span data-stu-id="a37d8-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-142">Ostatní</span><span class="sxs-lookup"><span data-stu-id="a37d8-142">Other</span></span></p></td>
<td><p><span data-ttu-id="a37d8-143">AI</span><span class="sxs-lookup"><span data-stu-id="a37d8-143">AI</span></span></p></td>
<td><p><span data-ttu-id="a37d8-144">Použít jako</span><span class="sxs-lookup"><span data-stu-id="a37d8-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-145">Jiná</span><span class="sxs-lookup"><span data-stu-id="a37d8-145">Other</span></span></p></td>
<td><p><span data-ttu-id="a37d8-146">RS</span><span class="sxs-lookup"><span data-stu-id="a37d8-146">RS</span></span></p></td>
<td><p><span data-ttu-id="a37d8-147">Opětovný prodej</span><span class="sxs-lookup"><span data-stu-id="a37d8-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-148">Jiná</span><span class="sxs-lookup"><span data-stu-id="a37d8-148">Other</span></span></p></td>
<td><p><span data-ttu-id="a37d8-149">EX</span><span class="sxs-lookup"><span data-stu-id="a37d8-149">EX</span></span></p></td>
<td><p><span data-ttu-id="a37d8-150">Směna</span><span class="sxs-lookup"><span data-stu-id="a37d8-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-151">Jiná</span><span class="sxs-lookup"><span data-stu-id="a37d8-151">Other</span></span></p></td>
<td><p><span data-ttu-id="a37d8-152">MS</span><span class="sxs-lookup"><span data-stu-id="a37d8-152">MS</span></span></p></td>
<td><p><span data-ttu-id="a37d8-153">Různé</span><span class="sxs-lookup"><span data-stu-id="a37d8-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a37d8-154">Pro každý kód dispozice, který definujete, je nutné vybrat dispoziční akci.</span><span class="sxs-lookup"><span data-stu-id="a37d8-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="a37d8-155">Dispoziční akce určují fyzické a finanční důsledky dispozičních kódů.</span><span class="sxs-lookup"><span data-stu-id="a37d8-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="a37d8-156">Dispoziční akce například určuje fyzické zpracování vráceného zboží, finanční dopad vráceného zboží a informaci o tom, zda má být odběrateli zasláno náhradní zboží.</span><span class="sxs-lookup"><span data-stu-id="a37d8-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="a37d8-157">Můžete definovat neomezený počet dispozičních kódů podle vašich obchodních potřeb, ale existuje pouze šest předdefinovaných dispozičních akcí, které lze vybírat.</span><span class="sxs-lookup"><span data-stu-id="a37d8-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="a37d8-158">Následující tabulka obsahuje dispoziční akce a jejich definice.</span><span class="sxs-lookup"><span data-stu-id="a37d8-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a37d8-159">Dispoziční akce</span><span class="sxs-lookup"><span data-stu-id="a37d8-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="a37d8-160">popis</span><span class="sxs-lookup"><span data-stu-id="a37d8-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-161"><strong>Kreditní</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-162">Vrácení zboží do skladové zásoby a vrácení peněz odběrateli.</span><span class="sxs-lookup"><span data-stu-id="a37d8-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-163"><strong>Pouze Dal</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-164">Vrácení peněz odběrateli bez vyžadování či očekávání návratu zboží.</span><span class="sxs-lookup"><span data-stu-id="a37d8-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-165"><strong>Odpad</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-166">Likvidace zboží a vrácení peněz odběrateli.</span><span class="sxs-lookup"><span data-stu-id="a37d8-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-167"><strong>Nahradit a připsat na stranu Dal</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-168">Vrácení zboží do skladové zásoby, vytvoření náhradní objednávky a vrácení peněz odběrateli.</span><span class="sxs-lookup"><span data-stu-id="a37d8-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a37d8-169"><strong>Nahradit a vyřadit</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-170">Likvidace zboží, vytvoření náhradní objednávky a vrácení peněz odběrateli.</span><span class="sxs-lookup"><span data-stu-id="a37d8-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a37d8-171"><strong>Vrátit odběrateli</strong></span><span class="sxs-lookup"><span data-stu-id="a37d8-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="a37d8-172">Odmítnutí vráceného zboží a jeho vrácení zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="a37d8-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="a37d8-173">Vyberte dispoziční kód pro karanténní příkaz.</span><span class="sxs-lookup"><span data-stu-id="a37d8-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="a37d8-174">Klikněte na **Řízení zásob** \> **Periodicky** \> **Správa kvality** \> **Karanténní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="a37d8-175">Pro stávající karanténní příkaz vyberte akci v poli **Dispoziční kód** na kartě **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="a37d8-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="a37d8-176">Viz také</span><span class="sxs-lookup"><span data-stu-id="a37d8-176">See also</span></span>

<span data-ttu-id="a37d8-177">[Karanténní příkaz (formulář)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="a37d8-177">[Quarantine order (form)](https://technet.microsoft.com/en-us/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="a37d8-178">[Dispoziční kódy (formulář)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a37d8-178">[Disposition codes (form)](https://technet.microsoft.com/en-us/library/hh597113\(v=ax.60\))</span></span>

  


