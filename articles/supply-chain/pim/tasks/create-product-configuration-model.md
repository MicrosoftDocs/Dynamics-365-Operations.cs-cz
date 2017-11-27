--- 
title: "Vytvoření modelu konfigurace produktu"
description: "Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: d494a20ba6f1f9c33a3935779b4bd3a8eefce26a
ms.contentlocale: cs-cz
ms.lasthandoff: 11/14/2017

---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="328c5-103">Vytvoření modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="328c5-103">Create a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="328c5-104">Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty.</span><span class="sxs-lookup"><span data-stu-id="328c5-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="328c5-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="328c5-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="328c5-106">Vytvoření modelu výrobku</span><span class="sxs-lookup"><span data-stu-id="328c5-106">Create a product model</span></span>
1. <span data-ttu-id="328c5-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="328c5-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="328c5-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="328c5-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="328c5-109">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="328c5-109">Click New.</span></span>
4. <span data-ttu-id="328c5-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="328c5-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="328c5-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="328c5-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="328c5-112">Vyberte volbu v poli Strategie řešitele.</span><span class="sxs-lookup"><span data-stu-id="328c5-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="328c5-113">Strategie řešitele určuje způsob zpracování omezení v modelu konfigurace produktu založeného na omezeních.</span><span class="sxs-lookup"><span data-stu-id="328c5-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="328c5-114">Tento výběr může mít vliv na výkon modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="328c5-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="328c5-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="328c5-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="328c5-116">Kořenová komponenta představuje model konfigurace produktu, ale lze ji použít také v jiných modelech výrobků.</span><span class="sxs-lookup"><span data-stu-id="328c5-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="328c5-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="328c5-117">Click OK.</span></span>
9. <span data-ttu-id="328c5-118">V poli Znovu použít konfigurace vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="328c5-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="328c5-119">Je-li parametr opakovaného použití konfigurace nastaven na hodnotu Ano, systém zkontroluje v každé konfigurační relaci, zda byla nalezena identická konfigurace, a pokud byla nalezena přesná shoda, použije ji znovu.</span><span class="sxs-lookup"><span data-stu-id="328c5-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="328c5-120">Přidat atributy</span><span class="sxs-lookup"><span data-stu-id="328c5-120">Add attributes</span></span>
1. <span data-ttu-id="328c5-121">Rozbalte sekci Atributy.</span><span class="sxs-lookup"><span data-stu-id="328c5-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="328c5-122">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="328c5-122">Click Add.</span></span>
3. <span data-ttu-id="328c5-123">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="328c5-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="328c5-124">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="328c5-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="328c5-125">Do pole Název řešitele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="328c5-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="328c5-126">Název řešitele je používán řešitelem omezení konfigurátoru výrobku.</span><span class="sxs-lookup"><span data-stu-id="328c5-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="328c5-127">Nesmí obsahovat mezery ani speciální znaky kromě _ (podtržítko).</span><span class="sxs-lookup"><span data-stu-id="328c5-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="328c5-128">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="328c5-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="328c5-129">Text popis se zobrazí uživateli konfigurace, a může proto sloužit jako pomoc při výběru správné hodnoty atributu.</span><span class="sxs-lookup"><span data-stu-id="328c5-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="328c5-130">V poli Typ atributu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="328c5-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="328c5-131">Typ atributu určuje, které hodnoty jsou pro atribut k dispozici.</span><span class="sxs-lookup"><span data-stu-id="328c5-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="328c5-132">Zaškrtněte políčko položky Zahrnout do opakovaného použití.</span><span class="sxs-lookup"><span data-stu-id="328c5-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="328c5-133">Tato možnost je k dispozici pouze v případě, že je vybrána možnost Znovu použít konfigurace.</span><span class="sxs-lookup"><span data-stu-id="328c5-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="328c5-134">Zaškrtávací políčko Zahrnutí atributu do opětovného použití znamená, že tento atribut bude zvážen, když bude systém hledat přesnou shodu.</span><span class="sxs-lookup"><span data-stu-id="328c5-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="328c5-135">Přidat dílčí komponenty</span><span class="sxs-lookup"><span data-stu-id="328c5-135">Add subcomponents</span></span>
1. <span data-ttu-id="328c5-136">Rozbalte sekci Dílčí komponenty.</span><span class="sxs-lookup"><span data-stu-id="328c5-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="328c5-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="328c5-137">Click Add.</span></span>
3. <span data-ttu-id="328c5-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="328c5-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="328c5-139">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="328c5-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="328c5-140">Do pole Název řešitele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="328c5-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="328c5-141">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="328c5-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="328c5-142">V poli Komponenty zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="328c5-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="328c5-143">Každý dílčí komponent musí odkazovat na definici komponenty.</span><span class="sxs-lookup"><span data-stu-id="328c5-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="328c5-144">Tento návrh podporuje opakované použití komponent a zajišťuje, že po definování komponenty ji je možné použít v mnoha modelech výrobků.</span><span class="sxs-lookup"><span data-stu-id="328c5-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="328c5-145">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="328c5-145">Click Save.</span></span>
9. <span data-ttu-id="328c5-146">Klepněte na podrobnosti řádku kusovníku.</span><span class="sxs-lookup"><span data-stu-id="328c5-146">Click BOM line details.</span></span>
    * <span data-ttu-id="328c5-147">Formulář Podrobnosti řádku Kusovníku umožňuje uživatelům vybrat požadované vlastnosti pro dílčí komponentu.</span><span class="sxs-lookup"><span data-stu-id="328c5-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="328c5-148">Všechny vlastnosti mohou mít stanovenou pevnou hodnotu nebo namapovanou hodnotu k atributu.</span><span class="sxs-lookup"><span data-stu-id="328c5-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="328c5-149">Mapování na atribut má za výsledek, že vlastnosti řádku kusovníku získají odlišné hodnoty v závislosti na výběru konfigurace.</span><span class="sxs-lookup"><span data-stu-id="328c5-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="328c5-150">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="328c5-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="328c5-151">Každý dílčí představuje základní konfigurovatelný produkt s technologií konfigurace založenou na omezeních.</span><span class="sxs-lookup"><span data-stu-id="328c5-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="328c5-152">Odkaz je vytvořen prostřednictvím čísla položky.</span><span class="sxs-lookup"><span data-stu-id="328c5-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="328c5-153">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="328c5-153">Select the Set check box.</span></span>
12. <span data-ttu-id="328c5-154">Vyberte možnost Ano v poli Výpočet.</span><span class="sxs-lookup"><span data-stu-id="328c5-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="328c5-155">Možnost nastavení výpočtu zajišťuje, že výrobek bude zahrnut při spuštění výpočtu nákladů pro produkt.</span><span class="sxs-lookup"><span data-stu-id="328c5-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="328c5-156">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="328c5-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="328c5-157">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="328c5-157">Select the Set check box.</span></span>
15. <span data-ttu-id="328c5-158">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="328c5-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="328c5-159">Pole množství určuje, kolik tohoto produktu bude spotřebováno v konfigurovaném produktu.</span><span class="sxs-lookup"><span data-stu-id="328c5-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="328c5-160">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="328c5-160">Select the Set check box.</span></span>
17. <span data-ttu-id="328c5-161">V poli Podle sérií zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="328c5-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="328c5-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="328c5-162">Click OK.</span></span>


