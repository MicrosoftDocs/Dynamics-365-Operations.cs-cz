---
title: 'Definování procesu částečné cyklické inventury skladového místa '
description: Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě.
author: ShylaThompson
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3aafb42cea1664b0629f57fe4492736601902cc1
ms.sourcegitcommit: bacad87e2b9146e08e6fe16af01356954eb90574
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2019
ms.locfileid: "373388"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="233f8-103">Definování procesu částečné cyklické inventury skladového místa </span><span class="sxs-lookup"><span data-stu-id="233f8-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="233f8-104">Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="233f8-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="233f8-105">Vyfiltrováním konkrétních produktů může vedoucí skladu snížit kontrolu režie, vyhnout se chybám konsolidace a ušetřit čas.</span><span class="sxs-lookup"><span data-stu-id="233f8-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="233f8-106">Vedoucí skladu obvykle provádí nastavení.</span><span class="sxs-lookup"><span data-stu-id="233f8-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="233f8-107">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="233f8-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="233f8-108">Vytvoření šablony práce cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="233f8-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="233f8-109">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="233f8-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="233f8-110">V poli Typ pořadí pracovních činností vyberte možnost Cyklická inventura.</span><span class="sxs-lookup"><span data-stu-id="233f8-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="233f8-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="233f8-111">Click New.</span></span>
4. <span data-ttu-id="233f8-112">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="233f8-113">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="233f8-114">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="233f8-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="233f8-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="233f8-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="233f8-116">Zadejte hodnotu do pole Šablona práce.</span><span class="sxs-lookup"><span data-stu-id="233f8-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="233f8-117">Zadejte hodnotu do pole Popis pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="233f8-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="233f8-118">V poli ID fondu práce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="233f8-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="233f8-119">V poli Pracovní priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="233f8-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="233f8-120">Click Save.</span></span>
11. <span data-ttu-id="233f8-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="233f8-121">Click New.</span></span>
12. <span data-ttu-id="233f8-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="233f8-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="233f8-123">V poli Typ práce vyberte Inventura.</span><span class="sxs-lookup"><span data-stu-id="233f8-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="233f8-124">V poli ID pracovní třídy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="233f8-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="233f8-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="233f8-125">Click Save.</span></span>
16. <span data-ttu-id="233f8-126">Klikněte na Zalomení řádků práce.</span><span class="sxs-lookup"><span data-stu-id="233f8-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="233f8-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="233f8-127">Click New.</span></span>
18. <span data-ttu-id="233f8-128">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="233f8-129">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="233f8-130">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="233f8-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="233f8-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="233f8-131">Click Save.</span></span>
20. <span data-ttu-id="233f8-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="233f8-132">Close the page.</span></span>
21. <span data-ttu-id="233f8-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="233f8-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="233f8-134">Vytvoření plánu cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="233f8-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="233f8-135">Přejděte do Správce skladu > Nastavení > Cyklická inventura > Plány cyklických inventur.</span><span class="sxs-lookup"><span data-stu-id="233f8-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="233f8-136">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="233f8-136">Click New.</span></span>
3. <span data-ttu-id="233f8-137">Zadejte hodnotu do pole ID plánu cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="233f8-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="233f8-138">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="233f8-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="233f8-139">Do pole Maximální počet cyklických inventur zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="233f8-140">V poli Šablona práce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="233f8-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="233f8-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="233f8-141">Click New.</span></span>
8. <span data-ttu-id="233f8-142">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="233f8-143">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="233f8-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="233f8-144">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="233f8-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="233f8-145">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="233f8-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="233f8-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="233f8-146">Click Save.</span></span>
11. <span data-ttu-id="233f8-147">Klikněte na Definovat dotaz na produkt.</span><span class="sxs-lookup"><span data-stu-id="233f8-147">Click Define product query.</span></span>
12. <span data-ttu-id="233f8-148">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="233f8-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="233f8-149">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="233f8-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="233f8-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="233f8-150">Click OK.</span></span>
15. <span data-ttu-id="233f8-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="233f8-151">Close the page.</span></span>
