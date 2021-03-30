---
title: Nastavení šablony práce pro nákupní objednávky
description: Toto téma popisuje nastavení jednoduché pracovní šablony pro použití při odložení doručených položek.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe0b6f9b966a5ce31af9da74a2038877debd2e7c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215738"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="d641b-103">Nastavení šablony práce pro nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="d641b-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d641b-104">Toto téma popisuje nastavení jednoduché pracovní šablony pro použití při odložení doručených položek.</span><span class="sxs-lookup"><span data-stu-id="d641b-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="d641b-105">Šablony práce určují sadu pokynů představovanou pracovníkovi skladu na mobilním zařízení, zatímco jsou položky přesouvány z místa příjmu.</span><span class="sxs-lookup"><span data-stu-id="d641b-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="d641b-106">Můžete použít tuto proceduru s daty zmíněnými v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d641b-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="d641b-107">Před spuštěním tohoto průvodce vytvořte ID fondu práce.</span><span class="sxs-lookup"><span data-stu-id="d641b-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="d641b-108">V tomto příkladu se používá ID fondu práce nazvaný Příchozí.</span><span class="sxs-lookup"><span data-stu-id="d641b-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="d641b-109">Tento postup je určen pro vedoucího skladu.</span><span class="sxs-lookup"><span data-stu-id="d641b-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="d641b-110">V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Práce > Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="d641b-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="d641b-111">V poli **Typ pořadí pracovních činností** vyberte možnost **Nákupní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d641b-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="d641b-112">Nadpis vytvoření šablony práce</span><span class="sxs-lookup"><span data-stu-id="d641b-112">Create a work template header</span></span>
1. <span data-ttu-id="d641b-113">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d641b-113">Select **New**.</span></span>
2. <span data-ttu-id="d641b-114">V poli **Pořadové číslo** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d641b-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="d641b-115">Toto je pořadí, ve kterém jsou vyhodnoceny šablony práce.</span><span class="sxs-lookup"><span data-stu-id="d641b-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="d641b-116">Pořadí můžete v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="d641b-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="d641b-117">Zadejte hodnotu do pole **Šablona práce**.</span><span class="sxs-lookup"><span data-stu-id="d641b-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="d641b-118">Toto je jedinečný identifikátor pro tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="d641b-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="d641b-119">Zadejte hodnotu do pole **Popis pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="d641b-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="d641b-120">Možnost **Platná** nebude zaškrtnuta, dokud nedoplníte veškeré informace, které jsou nutné pro šablonu, a pak jste vybrali **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d641b-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="d641b-121">Pořadí pracovních činností typu **Nákupní objednávka** nelze zpracovat automaticky, proto ponechte možnost **Automatické zpracování** nastavenou na hodnotu **Ne**.</span><span class="sxs-lookup"><span data-stu-id="d641b-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="d641b-122">Zadejte hodnotu do pole **ID pracovního fondu**.</span><span class="sxs-lookup"><span data-stu-id="d641b-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="d641b-123">S ID fondů práce můžete uspořádat práci do skupin.</span><span class="sxs-lookup"><span data-stu-id="d641b-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="d641b-124">Hodnota nastavená v tomto poli se bude výchozí hodnotou pro všechnu práci vytvořenou pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="d641b-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="d641b-125">Do pole **Priorita práce** zadejte číslo `1`.</span><span class="sxs-lookup"><span data-stu-id="d641b-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="d641b-126">To ukazuje na význam práce a hodnoty, které nastavíte v tomto poli budou výchozí pro všechnu práci vytvořenou pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="d641b-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="d641b-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d641b-127">Select **Save**.</span></span> <span data-ttu-id="d641b-128">Předtím, než bude k dispozici tlačítko **Upravit dotaz**, musíte uložit záhlaví šablony práce.</span><span class="sxs-lookup"><span data-stu-id="d641b-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="d641b-129">Nastavit dotaz pro šablonu práce</span><span class="sxs-lookup"><span data-stu-id="d641b-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="d641b-130">Vyberte **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="d641b-130">Select **Edit query**.</span></span> <span data-ttu-id="d641b-131">Nastavíme omezení, že šablony lze použít jen v určitém skladu.</span><span class="sxs-lookup"><span data-stu-id="d641b-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="d641b-132">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="d641b-132">Select **Add**.</span></span>
3. <span data-ttu-id="d641b-133">Do pole **Pole** na novém řádku napište `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="d641b-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="d641b-134">Zadejte hodnotu do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="d641b-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="d641b-135">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d641b-135">Select **OK**.</span></span>
6. <span data-ttu-id="d641b-136">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d641b-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="d641b-137">Nastavit podrobnosti šablony práce</span><span class="sxs-lookup"><span data-stu-id="d641b-137">Set work template details</span></span>
1. <span data-ttu-id="d641b-138">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d641b-138">Select **New**.</span></span>
2. <span data-ttu-id="d641b-139">V poli **Typ práce** vyberte **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="d641b-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="d641b-140">Zadejte `purchase` do pole **ID pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="d641b-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="d641b-141">Pracovní třída, kterou nastavíte zde, bude výchozí pro všechny řádky práce typu Výdej, vytvořené pomocí této šablony.</span><span class="sxs-lookup"><span data-stu-id="d641b-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="d641b-142">Třída práce nemůže být přepsána z řádků pořadí pracovních činností.</span><span class="sxs-lookup"><span data-stu-id="d641b-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="d641b-143">Pracovní třídy se používají k nasměrování a/nebo omezení typu řádků pracovních objednávek, které pracovník skladu dokáže v mobilním zařízení zpracovat.</span><span class="sxs-lookup"><span data-stu-id="d641b-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="d641b-144">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d641b-144">Select **New**.</span></span>
5. <span data-ttu-id="d641b-145">V poli **Typ práce** vyberte **Vložit**.</span><span class="sxs-lookup"><span data-stu-id="d641b-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="d641b-146">Do pole **ID pracovní třídy** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d641b-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="d641b-147">Jsou nastaveny pokyny pro výdej a příjem.</span><span class="sxs-lookup"><span data-stu-id="d641b-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="d641b-148">Každá sada výdej/příjmu musí mít stejnou pracovní třídu.</span><span class="sxs-lookup"><span data-stu-id="d641b-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="d641b-149">Používejte stejnou pracovní třídu, kterou jste zadali pro instrukci výdeje.</span><span class="sxs-lookup"><span data-stu-id="d641b-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="d641b-150">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="d641b-150">Select **Save**.</span></span> <span data-ttu-id="d641b-151">Všimněte si, že je nyní zaškrtnuto zaškrtávací políčko **Platné**.</span><span class="sxs-lookup"><span data-stu-id="d641b-151">Note that the **Valid** checkbox is now checked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]