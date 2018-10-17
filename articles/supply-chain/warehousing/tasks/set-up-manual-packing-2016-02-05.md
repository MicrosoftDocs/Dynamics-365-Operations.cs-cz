--- 
title: "Nastavení ručního balení (únor 2016 a květen 2016)"
description: "Proces balení umožňuje ověřit a zabalit produkty do kontejnerů."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: b90b4a71e2447e942dbb4a9645ef93064da630d3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="7c6cf-103">Nastavení ručního balení (únor 2016 a květen 2016)</span><span class="sxs-lookup"><span data-stu-id="7c6cf-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c6cf-104">Proces balení umožňuje ověřit a zabalit produkty do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="7c6cf-105">V tomto procesu pracovníci skladu vyskladní produkty z umístění úložiště je přesunou je do stanice balení, kde zkontrolují množství a typy položek a přiřadí je k příslušným kontejnerům.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="7c6cf-106">Po plném zabalení kontejneru jej mohou uzavřít a přesunout do výstupního překladiště, kde jsou produkty připraveny k expedici.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="7c6cf-107">Tato procedura používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="7c6cf-108">Tato procedura je určena pouze pro verze aplikace Dynamics 365 for Operations na únor 2016 a květen 2016.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="7c6cf-109">Nastavit profily skladových míst</span><span class="sxs-lookup"><span data-stu-id="7c6cf-109">Set up location profiles</span></span>
1. <span data-ttu-id="7c6cf-110">Přejděte do nabídky Řízení skladu > Nastavení > Sklad > Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="7c6cf-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-111">Click New.</span></span>
    * <span data-ttu-id="7c6cf-112">Profil místa se používá pro stanice balení a obsahuje informace a pravidla pro umístění.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="7c6cf-113">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="7c6cf-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7c6cf-115">V poli Formát skladového místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="7c6cf-116">V poli Typ místa zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="7c6cf-117">Vyberte možnost Ano v poli Povolit smíšené položky.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="7c6cf-118">Vyberte možnost Ano v poli Povolit smíšené stavy zásob.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="7c6cf-119">Vyberte možnost Ano v poli Pravidla přepisu pro dny dávky.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="7c6cf-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="7c6cf-121">Nastavení parametrů pro řízení skladu</span><span class="sxs-lookup"><span data-stu-id="7c6cf-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="7c6cf-122">Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="7c6cf-123">Klikněte na kartu Balení.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="7c6cf-124">V poli ID profilu pro umístění balení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="7c6cf-125">Vyberte profil umístění, který chcete použít pro balení.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="7c6cf-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="7c6cf-127">Nastavení typů kontejneru</span><span class="sxs-lookup"><span data-stu-id="7c6cf-127">Set up container types</span></span>
1. <span data-ttu-id="7c6cf-128">Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="7c6cf-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-129">Click New.</span></span>
    * <span data-ttu-id="7c6cf-130">Můžete definovat typy kontejnerů, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-130">You can define the types of containers to use.</span></span> <span data-ttu-id="7c6cf-131">Můžete zadat fyzické dimenze kontejneru, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="7c6cf-132">Vlastnosti jsou upravená pole, která umožňují přidat další dimenze pro typ kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="7c6cf-133">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="7c6cf-134">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7c6cf-135">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="7c6cf-136">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="7c6cf-137">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="7c6cf-138">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="7c6cf-139">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="7c6cf-140">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="7c6cf-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-141">Click Save.</span></span>
12. <span data-ttu-id="7c6cf-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="7c6cf-143">Nastavení profilů balení</span><span class="sxs-lookup"><span data-stu-id="7c6cf-143">Set up packing profiles</span></span>
1. <span data-ttu-id="7c6cf-144">Přejděte do nabídky Řízení skladu > Nastavení > Balení > Profily balení.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="7c6cf-145">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-145">Click New.</span></span>
3. <span data-ttu-id="7c6cf-146">Zadejte hodnotu do pole ID profilu balení.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7c6cf-147">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7c6cf-148">V poli ID profilu uzávěrky kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="7c6cf-149">ID profilu uzávěrky kontejneru je volitelné a je výchozím profilem uzavřeného kontejneru pro tento profil balení.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="7c6cf-150">Vyberte volbu v poli ID režimu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="7c6cf-151">Tato možnost určuje, zda ID kontejneru bude automaticky generováno při vytvoření kontejneru, nebo zda je ID kontejneru vytvářeno ručně.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="7c6cf-152">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="7c6cf-153">Při vytvoření nového kontejneru se typ kontejneru použije jako výchozí.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="7c6cf-154">Označte pole Automaticky vytvořit kontejner při zavření kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="7c6cf-155">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-155">Click Save.</span></span>
10. <span data-ttu-id="7c6cf-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="7c6cf-157">Nastavení profilů uzávěrky kontejneru</span><span class="sxs-lookup"><span data-stu-id="7c6cf-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="7c6cf-158">Přejděte na Řízení skladu > Nastavení > Kontejnery > Profily uzávěrky kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="7c6cf-159">Profily uzávěrky kontejneru definují postup při uzavření kontejneru.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="7c6cf-160">Je možné nastavit více profilů pro zavřený kontejner.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="7c6cf-161">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-161">Click New.</span></span>
3. <span data-ttu-id="7c6cf-162">V poli ID profilu uzávěrky kontejneru zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="7c6cf-163">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7c6cf-164">Vyberte volbu v poli Manifest v.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="7c6cf-165">Určete, zda dojde k projevu při uzávěrce kontejneru nebo při potvrzení expedice.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="7c6cf-166">Všimněte si, že projev vyžaduje správu přepravy.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="7c6cf-167">Projev musí být implementován v modulech přepravy, aby je bylo možné používat.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="7c6cf-168">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="7c6cf-169">V poli Výchozí umístění pro konečnou dodávku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="7c6cf-170">To bude umístění, kam budou přesunuty produkty, jakmile budou kontejnery uzavřené.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="7c6cf-171">Toto skladové místo musí mít profil skladového místa definováno v parametrech skladu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="7c6cf-172">V poli Hmotnost jednotky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="7c6cf-173">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7c6cf-173">Click Save.</span></span>


