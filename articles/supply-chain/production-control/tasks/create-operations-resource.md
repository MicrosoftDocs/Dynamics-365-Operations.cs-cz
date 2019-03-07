---
title: Vytvoření provozního prostředku
description: Provozní prostředek provádí aktivity projektu nebo výrobního procesu.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "350060"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="fb1fe-103">Vytvoření provozního prostředku</span><span class="sxs-lookup"><span data-stu-id="fb1fe-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb1fe-104">Provozní prostředek provádí aktivity projektu nebo výrobního procesu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="fb1fe-105">Tento postup popisuje postup definice provozního prostředku.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="fb1fe-106">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="fb1fe-107">Přejděte na Prostředky.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-107">Go to Resources.</span></span>
2. <span data-ttu-id="fb1fe-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-108">Click New.</span></span>
3. <span data-ttu-id="fb1fe-109">Zadejte hodnotu do pole Prostředek.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="fb1fe-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="fb1fe-111">Definování parametrů kapacity a spotřeby</span><span class="sxs-lookup"><span data-stu-id="fb1fe-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="fb1fe-112">Rozbalte sekci Operace.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="fb1fe-113">V poli Podíl odpadu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="fb1fe-114">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="fb1fe-115">Určete nákladovou kategorii, která určuje, jak nakládat s účtem pro náklady spojené s nastavením.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="fb1fe-116">V Kategorie operačního času zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="fb1fe-117">Určete nákladovou kategorii, která určuje, jak nakládat s účtem pro náklady spojené s provozem.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="fb1fe-118">V Kategorie množství zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="fb1fe-119">Určete nákladovou kategorii definující způsob nakládání s účtem pro náklady spojené s prostředky na základě výstupního množství.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="fb1fe-120">V poli Jednotka kapacity vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="fb1fe-121">Zadejte jednotku, ve které se má vyjádřit kapacita provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="fb1fe-122">V poli Kapacita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="fb1fe-123">V poli Procento účinnosti je třeba zadat číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="fb1fe-124">Určete účinnost, kterou očekáváte od provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="fb1fe-125">Procenta účinnosti upraví propustnosti provozních prostředků a má vliv na dobu rezervovanou pro prostředek.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="fb1fe-126">V poli Procento plánování operací zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="fb1fe-127">Zadejte maximální procento kapacity provozního prostředku, kterou chcete použít při plánování operací.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="fb1fe-128">Vyberte Ano v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="fb1fe-129">Nastavte možnost Ano v případě, že provozní prostředek má být naplánován podle skutečné dostupné kapacitě, a pokud by se měly zvážit existující rezervace kapacity.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="fb1fe-130">Je-li tato možnost je nastavena na hodnotu Ne, u provozního prostředku se předpokládá, že je nastavena neomezená kapacita, a zdroj může být přeplněn.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="fb1fe-131">Vyberte možnost Ano v poli Kritický prostředek.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="fb1fe-132">Definování pracovní doby</span><span class="sxs-lookup"><span data-stu-id="fb1fe-132">Define working times</span></span>
1. <span data-ttu-id="fb1fe-133">Rozbalte sekci Kalendáře.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="fb1fe-134">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-134">Click Add.</span></span>
3. <span data-ttu-id="fb1fe-135">V poli Kalendář zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="fb1fe-136">Určete kalendář pracovní doby, který definuje kapacitu prostředků (v hodinách).</span><span class="sxs-lookup"><span data-stu-id="fb1fe-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="fb1fe-137">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="fb1fe-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="fb1fe-139">Definování schopností prostředku</span><span class="sxs-lookup"><span data-stu-id="fb1fe-139">Define resource capabilities</span></span>
1. <span data-ttu-id="fb1fe-140">Rozbalte sekci Schopnosti.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="fb1fe-141">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-141">Click Add.</span></span>
    * <span data-ttu-id="fb1fe-142">Schopnost je možnost provozních prostředků provádět určitou aktivitu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="fb1fe-143">Plánovací modul přidělí prostředky spárováním provozních prostředků jednotlivých aktivit s možnostmi dostupných provozních prostředků.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="fb1fe-144">V poli Schopnost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="fb1fe-145">Do pole Úroveň zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="fb1fe-146">Určete úroveň způsobilosti, podle které prostředek zpracuje schopnost.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="fb1fe-147">V poli Priorita zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="fb1fe-148">Určete prioritu provozního prostředku s ohledem na schopnost.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="fb1fe-149">Při plánování podle priority nejprve vyberte provozní prostředky s nejvyšší prioritou (nejnižší číslo).</span><span class="sxs-lookup"><span data-stu-id="fb1fe-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="fb1fe-150">Přiřazení prostředku ke skupině prostředků</span><span class="sxs-lookup"><span data-stu-id="fb1fe-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="fb1fe-151">Rozbalte sekci Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="fb1fe-152">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-152">Click Add.</span></span>
    * <span data-ttu-id="fb1fe-153">Skupina prostředků definuje pracoviště, výrobní jednotku a kontext skladu pro provozní prostředek.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="fb1fe-154">Provozní prostředek může být naplánován pouze pokud byl přiřazen ke skupině prostředků, a pouze na pracoviště, kde je umístěna skupina prostředků.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="fb1fe-155">V poli Skupina prostředků zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="fb1fe-156">V poli Vstupní místo zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="fb1fe-157">Zadejte umístění ve skladu, ze kterého provozní prostředek spotřebovává materiál.</span><span class="sxs-lookup"><span data-stu-id="fb1fe-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

