--- 
title: "Nastavení ručního balení (jen ve verzi z února 2016 a května 2016)"
description: "Proces balení umožňuje ověřit a zabalit produkty do kontejnerů."
author: ShylaThompson
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7e776a08ec2adc48b77c86c16e1f291e524a8d00
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="01abb-103">Nastavení ručního balení (jen ve verzi z února 2016 a května 2016)</span><span class="sxs-lookup"><span data-stu-id="01abb-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01abb-104">Proces balení umožňuje ověřit a zabalit produkty do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="01abb-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="01abb-105">V tomto procesu pracovníci skladu vyskladní produkty z umístění úložiště je přesunou je do stanice balení, kde zkontrolují množství a typy položek a přiřadí je k příslušným kontejnerům.</span><span class="sxs-lookup"><span data-stu-id="01abb-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="01abb-106">Po plném zabalení kontejneru jej mohou uzavřít a přesunout do výstupního překladiště, kde jsou produkty připraveny k expedici.</span><span class="sxs-lookup"><span data-stu-id="01abb-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="01abb-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="01abb-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="01abb-108">Nastavit profily skladových míst</span><span class="sxs-lookup"><span data-stu-id="01abb-108">Set up location profiles</span></span>
1. <span data-ttu-id="01abb-109">Přejděte do nabídky Řízení skladu > Nastavení > Sklad > Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="01abb-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="01abb-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01abb-110">Click New.</span></span>
    * <span data-ttu-id="01abb-111">Profil místa se používá pro stanice balení a obsahuje informace a pravidla pro umístění.</span><span class="sxs-lookup"><span data-stu-id="01abb-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="01abb-112">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="01abb-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="01abb-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="01abb-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="01abb-114">V poli Formát skladového místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="01abb-115">V poli Typ místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="01abb-116">Vyberte možnost Ano v poli Povolit smíšené položky.</span><span class="sxs-lookup"><span data-stu-id="01abb-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="01abb-117">Vyberte možnost Ano v poli Povolit smíšené stavy zásob.</span><span class="sxs-lookup"><span data-stu-id="01abb-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="01abb-118">Vyberte možnost Ano v poli Pravidla přepisu pro dny dávky.</span><span class="sxs-lookup"><span data-stu-id="01abb-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="01abb-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01abb-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="01abb-120">Nastavení parametrů pro řízení skladu</span><span class="sxs-lookup"><span data-stu-id="01abb-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="01abb-121">Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="01abb-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="01abb-122">Klikněte na kartu Balení.</span><span class="sxs-lookup"><span data-stu-id="01abb-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="01abb-123">V poli ID profilu pro umístění balení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="01abb-124">Vyberte profil umístění, který chcete použít pro balení.</span><span class="sxs-lookup"><span data-stu-id="01abb-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="01abb-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01abb-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="01abb-126">Nastavení typů kontejneru</span><span class="sxs-lookup"><span data-stu-id="01abb-126">Set up container types</span></span>
1. <span data-ttu-id="01abb-127">Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="01abb-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="01abb-128">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01abb-128">Click New.</span></span>
    * <span data-ttu-id="01abb-129">Můžete definovat typy kontejnerů, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="01abb-129">You can define the types of containers to use.</span></span> <span data-ttu-id="01abb-130">Můžete zadat fyzické dimenze kontejneru, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="01abb-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="01abb-131">Vlastnosti jsou upravená pole, která umožňují přidat další dimenze pro typ kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="01abb-132">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="01abb-133">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="01abb-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01abb-134">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01abb-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="01abb-135">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="01abb-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="01abb-136">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01abb-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="01abb-137">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01abb-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="01abb-138">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01abb-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="01abb-139">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01abb-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="01abb-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01abb-140">Click Save.</span></span>
12. <span data-ttu-id="01abb-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01abb-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="01abb-142">Nastavení profilů balení</span><span class="sxs-lookup"><span data-stu-id="01abb-142">Set up packing profiles</span></span>
1. <span data-ttu-id="01abb-143">Přejděte do nabídky Řízení skladu > Nastavení > Balení > Profily balení.</span><span class="sxs-lookup"><span data-stu-id="01abb-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="01abb-144">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01abb-144">Click New.</span></span>
3. <span data-ttu-id="01abb-145">Zadejte hodnotu do pole ID profilu balení.</span><span class="sxs-lookup"><span data-stu-id="01abb-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="01abb-146">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="01abb-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01abb-147">V poli ID profilu uzávěrky kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="01abb-148">ID profilu uzávěrky kontejneru je volitelné a je výchozím profilem uzavřeného kontejneru pro tento profil balení.</span><span class="sxs-lookup"><span data-stu-id="01abb-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="01abb-149">Vyberte volbu v poli ID režimu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="01abb-150">Tato možnost určuje, zda ID kontejneru bude automaticky generováno při vytvoření kontejneru, nebo zda je ID kontejneru vytvářeno ručně.</span><span class="sxs-lookup"><span data-stu-id="01abb-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="01abb-151">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="01abb-152">Při vytvoření nového kontejneru se typ kontejneru použije jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="01abb-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="01abb-153">Označte pole Automaticky vytvořit kontejner při zavření kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="01abb-154">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01abb-154">Click Save.</span></span>
10. <span data-ttu-id="01abb-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01abb-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="01abb-156">Nastavení profilů uzávěrky kontejneru</span><span class="sxs-lookup"><span data-stu-id="01abb-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="01abb-157">Přejděte na Řízení skladu > Nastavení > Kontejnery > Profily uzávěrky kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="01abb-158">Profily uzávěrky kontejneru definují postup při uzavření kontejneru.</span><span class="sxs-lookup"><span data-stu-id="01abb-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="01abb-159">Je možné nastavit více profilů pro zavřený kontejner.</span><span class="sxs-lookup"><span data-stu-id="01abb-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="01abb-160">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01abb-160">Click New.</span></span>
3. <span data-ttu-id="01abb-161">V poli ID profilu uzávěrky kontejneru zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="01abb-162">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="01abb-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="01abb-163">Vyberte volbu v poli Manifest v.</span><span class="sxs-lookup"><span data-stu-id="01abb-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="01abb-164">Určete, zda dojde k projevu při uzávěrce kontejneru nebo při potvrzení expedice.</span><span class="sxs-lookup"><span data-stu-id="01abb-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="01abb-165">Všimněte si, že projev vyžaduje správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="01abb-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="01abb-166">Projev musí být implementován v modulech přepravy, aby je bylo možné používat.</span><span class="sxs-lookup"><span data-stu-id="01abb-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="01abb-167">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="01abb-168">V poli Výchozí umístění pro konečnou dodávku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="01abb-169">To bude umístění, kam budou přesunuty produkty, jakmile budou kontejnery uzavřené.</span><span class="sxs-lookup"><span data-stu-id="01abb-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="01abb-170">Toto skladové místo musí mít profil skladového místa definováno v parametrech skladu.</span><span class="sxs-lookup"><span data-stu-id="01abb-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="01abb-171">V poli Hmotnost jednotky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="01abb-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="01abb-172">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01abb-172">Click Save.</span></span>


