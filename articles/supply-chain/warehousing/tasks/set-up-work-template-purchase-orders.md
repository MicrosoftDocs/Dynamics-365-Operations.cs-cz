--- 
title: "Nastavení šablony práce pro nákupní objednávky"
description: "Tento postup se zaměřuje na nastavení jednoduché pracovní šablony pro použití při odložení doručených položek."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1bd59ffca94c57ad33f78f9e780d00b368750bc8
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="b8ea5-103">Nastavení šablony práce pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="b8ea5-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8ea5-104">Tento postup se zaměřuje na nastavení jednoduché pracovní šablony pro použití při odložení doručených položek.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="b8ea5-105">Šablony práce určují sadu pokynů představovanou pracovníkovi skladu na mobilním zařízení, zatímco jsou položky přesouvány z místa příjmu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="b8ea5-106">Můžete použít tuto proceduru s daty zmíněnými v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="b8ea5-107">Před spuštěním tohoto průvodce vytvořte ID fondu práce.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="b8ea5-108">V tomto příkladu se používá ID fondu práce nazvaný Příchozí.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="b8ea5-109">Tento postup je určen pro vedoucího skladu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="b8ea5-110">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="b8ea5-111">V poli Typ pořadí pracovních činností vyberte možnost Nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="b8ea5-112">Nadpis vytvoření šablony práce</span><span class="sxs-lookup"><span data-stu-id="b8ea5-112">Create a work template header</span></span>
1. <span data-ttu-id="b8ea5-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-113">Click New.</span></span>
2. <span data-ttu-id="b8ea5-114">V poli Pořadové číslo zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="b8ea5-115">Toto je pořadí, ve kterém jsou vyhodnoceny šablony práce.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="b8ea5-116">Pořadí můžete v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="b8ea5-117">Zadejte hodnotu do pole Šablona práce.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="b8ea5-118">Toto je jedinečný identifikátor pro tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="b8ea5-119">Zadejte hodnotu do pole Popis pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="b8ea5-120">Možnost Platná možnost nebude zaškrtnuta, dokud nedoplníte veškeré informace, které jsou nutné pro šablonu, a pak jste klepnuli na možnost Uložit.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="b8ea5-121">Pořadí pracovních činností typu Nákupní objednávka nelze zpracovat automaticky, proto ponechte možnost automatického zpracování nastavenou na hodnotu Ne.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="b8ea5-122">Zadejte hodnotu do pole ID pracovního fondu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="b8ea5-123">S ID fondů práce můžete uspořádat práci do skupin.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="b8ea5-124">Hodnota nastavená v tomto poli se bude výchozí hodnotou pro všechnu práci vytvořenou pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="b8ea5-125">Do pole Priorita práce zadejte číslo „1“.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="b8ea5-126">To ukazuje na význam práce a hodnoty, které nastavíte v tomto poli budou výchozí pro všechnu práci vytvořenou pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="b8ea5-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-127">Click Save.</span></span>
    * <span data-ttu-id="b8ea5-128">Předtím, než bude k dispozici tlačítko Upravit dotaz, musíte uložit záhlaví šablony práce.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="b8ea5-129">Nastavit dotaz pro šablonu práce</span><span class="sxs-lookup"><span data-stu-id="b8ea5-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="b8ea5-130">Klikněte na možnost Upravit dotaz.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-130">Click Edit query.</span></span>
    * <span data-ttu-id="b8ea5-131">Nastavíme omezení, že šablony lze použít jen v určitém skladu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="b8ea5-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-132">Click Add.</span></span>
3. <span data-ttu-id="b8ea5-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b8ea5-134">Do pole Pole zadejte „sklad“.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="b8ea5-135">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="b8ea5-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-136">Click OK.</span></span>
7. <span data-ttu-id="b8ea5-137">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="b8ea5-138">Nastavit podrobnosti šablony práce</span><span class="sxs-lookup"><span data-stu-id="b8ea5-138">Set work template details</span></span>
1. <span data-ttu-id="b8ea5-139">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-139">Click New.</span></span>
2. <span data-ttu-id="b8ea5-140">V poli Typ práce vyberte „Vybrat“.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="b8ea5-141">Zadejte „nákup“ do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="b8ea5-142">Pracovní třída, kterou nastavíte zde, bude výchozí pro všechny řádky práce typu Výdej, vytvořené pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="b8ea5-143">Třída práce nemůže být přepsána z řádků pořadí pracovních činností.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="b8ea5-144">Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních objednávek, které pracovník skladu dokáže v mobilním zařízení zpracovat.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="b8ea5-145">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-145">Click New.</span></span>
5. <span data-ttu-id="b8ea5-146">V poli Typ práce vyberte „Vložit“.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="b8ea5-147">Zadejte hodnotu do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="b8ea5-148">Jsou nastaveny pokyny pro výdej a příjem.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="b8ea5-149">Každá sada výdej/příjmu musí mít stejnou pracovní třídu.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="b8ea5-150">Používejte stejnou pracovní třídu, kterou jste zadali pro instrukci výdeje.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="b8ea5-151">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-151">Click Save.</span></span>
    * <span data-ttu-id="b8ea5-152">Všimněte si, že je nyní zaškrtnuto platné zaškrtávací políčko.</span><span class="sxs-lookup"><span data-stu-id="b8ea5-152">Note that the Valid checkbox is now checked.</span></span>  


