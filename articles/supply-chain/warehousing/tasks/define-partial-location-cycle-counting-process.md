---
title: 'Definování procesu částečné cyklické inventury skladového místa '
description: Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39a256a5a88a6d70373d6e23f1f380da6791f418
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424146"
---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="bee01-103">Definování procesu částečné cyklické inventury skladového místa </span><span class="sxs-lookup"><span data-stu-id="bee01-103">Define partial location cycle counting process</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bee01-104">Při použití plánů cyklických inventur pro vytvoření inventury můžete řídit vlastní inventurní operace vyžádáním pouze konkrétních produktů a variant produktů namísto všech zásob na skladě ve skladovém místě.</span><span class="sxs-lookup"><span data-stu-id="bee01-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="bee01-105">Vyfiltrováním konkrétních produktů může vedoucí skladu snížit kontrolu režie, vyhnout se chybám konsolidace a ušetřit čas.</span><span class="sxs-lookup"><span data-stu-id="bee01-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="bee01-106">Vedoucí skladu obvykle provádí nastavení.</span><span class="sxs-lookup"><span data-stu-id="bee01-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="bee01-107">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="bee01-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="bee01-108">Vytvoření šablony práce cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="bee01-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="bee01-109">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="bee01-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="bee01-110">V poli Typ pořadí pracovních činností vyberte možnost Cyklická inventura.</span><span class="sxs-lookup"><span data-stu-id="bee01-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="bee01-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bee01-111">Click New.</span></span>
4. <span data-ttu-id="bee01-112">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bee01-113">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bee01-114">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="bee01-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="bee01-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="bee01-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bee01-116">Zadejte hodnotu do pole Šablona práce.</span><span class="sxs-lookup"><span data-stu-id="bee01-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="bee01-117">Zadejte hodnotu do pole Popis pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="bee01-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="bee01-118">V poli ID fondu práce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bee01-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="bee01-119">V poli Pracovní priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="bee01-120">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bee01-120">Click Save.</span></span>
11. <span data-ttu-id="bee01-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bee01-121">Click New.</span></span>
12. <span data-ttu-id="bee01-122">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="bee01-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bee01-123">V poli Typ práce vyberte Inventura.</span><span class="sxs-lookup"><span data-stu-id="bee01-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="bee01-124">V poli ID pracovní třídy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bee01-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="bee01-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bee01-125">Click Save.</span></span>
16. <span data-ttu-id="bee01-126">Klikněte na Zalomení řádků práce.</span><span class="sxs-lookup"><span data-stu-id="bee01-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="bee01-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bee01-127">Click New.</span></span>
18. <span data-ttu-id="bee01-128">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bee01-129">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bee01-130">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="bee01-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="bee01-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bee01-131">Click Save.</span></span>
20. <span data-ttu-id="bee01-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bee01-132">Close the page.</span></span>
21. <span data-ttu-id="bee01-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bee01-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="bee01-134">Vytvoření plánu cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="bee01-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="bee01-135">Přejděte do Správce skladu > Nastavení > Cyklická inventura > Plány cyklických inventur.</span><span class="sxs-lookup"><span data-stu-id="bee01-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="bee01-136">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bee01-136">Click New.</span></span>
3. <span data-ttu-id="bee01-137">Zadejte hodnotu do pole ID plánu cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="bee01-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="bee01-138">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="bee01-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bee01-139">Do pole Maximální počet cyklických inventur zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="bee01-140">V poli Šablona práce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bee01-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="bee01-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bee01-141">Click New.</span></span>
8. <span data-ttu-id="bee01-142">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="bee01-143">Pořadí řazení je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="bee01-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="bee01-144">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="bee01-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="bee01-145">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="bee01-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="bee01-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bee01-146">Click Save.</span></span>
11. <span data-ttu-id="bee01-147">Klikněte na Definovat dotaz na produkt.</span><span class="sxs-lookup"><span data-stu-id="bee01-147">Click Define product query.</span></span>
12. <span data-ttu-id="bee01-148">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="bee01-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="bee01-149">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bee01-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="bee01-150">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bee01-150">Click OK.</span></span>
15. <span data-ttu-id="bee01-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bee01-151">Close the page.</span></span>

