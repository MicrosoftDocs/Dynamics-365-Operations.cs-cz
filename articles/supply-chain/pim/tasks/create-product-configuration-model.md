---
title: Vytvoření modelu konfigurace produktu
description: Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921358"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="7a72b-103">Vytvoření modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="7a72b-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a72b-104">Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty.</span><span class="sxs-lookup"><span data-stu-id="7a72b-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="7a72b-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="7a72b-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="7a72b-106">Vytvoření modelu výrobku</span><span class="sxs-lookup"><span data-stu-id="7a72b-106">Create a product model</span></span>

1. <span data-ttu-id="7a72b-107">Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="7a72b-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-108">Select **New**.</span></span>
1. <span data-ttu-id="7a72b-109">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7a72b-110">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="7a72b-111">Vyberte volbu v poli **Strategie řešitele**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="7a72b-112">Strategie řešitele určuje způsob zpracování omezení v modelu konfigurace produktu založeného na omezeních.</span><span class="sxs-lookup"><span data-stu-id="7a72b-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="7a72b-113">Tento výběr může mít vliv na výkon modelu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="7a72b-114">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="7a72b-115">Kořenová komponenta představuje model konfigurace produktu, ale lze ji použít také v jiných modelech výrobků.</span><span class="sxs-lookup"><span data-stu-id="7a72b-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="7a72b-116">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-116">Select **OK**.</span></span>
1. <span data-ttu-id="7a72b-117">V poli **Znovu použít konfigurace** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="7a72b-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="7a72b-118">Je-li parametr opakovaného použití konfigurace nastaven na hodnotu Ano, systém zkontroluje v každé konfigurační relaci, zda byla nalezena identická konfigurace, a pokud byla nalezena přesná shoda, použije ji znovu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="7a72b-119">Přidat atributy</span><span class="sxs-lookup"><span data-stu-id="7a72b-119">Add attributes</span></span>

1. <span data-ttu-id="7a72b-120">Rozbalte sekci **Atributy**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="7a72b-121">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-121">Select **Add**.</span></span>
3. <span data-ttu-id="7a72b-122">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="7a72b-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7a72b-123">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7a72b-124">Do pole **Název řešitele** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="7a72b-125">Název řešitele je používán řešitelem omezení konfigurátoru výrobku.</span><span class="sxs-lookup"><span data-stu-id="7a72b-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="7a72b-126">Nesmí obsahovat mezery ani speciální znaky kromě _ (podtržítko).</span><span class="sxs-lookup"><span data-stu-id="7a72b-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="7a72b-127">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="7a72b-128">Text popis se zobrazí uživateli konfigurace, a může proto sloužit jako pomoc při výběru správné hodnoty atributu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="7a72b-129">V poli **Typ atributu** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="7a72b-130">Typ atributu určuje, které hodnoty jsou pro atribut k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7a72b-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="7a72b-131">Zaškrtněte políčko položky **Zahrnout do opakovaného použití**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="7a72b-132">Tato možnost je k dispozici pouze v případě, že je vybrána možnost Znovu použít konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7a72b-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="7a72b-133">Zaškrtávací políčko Zahrnutí atributu do opětovného použití znamená, že tento atribut bude zvážen, když bude systém hledat přesnou shodu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="7a72b-134">Přidat dílčí komponenty</span><span class="sxs-lookup"><span data-stu-id="7a72b-134">Add subcomponents</span></span>

1. <span data-ttu-id="7a72b-135">Rozbalte sekci **Dílčí komponenty**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="7a72b-136">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-136">Select **Add**.</span></span>
3. <span data-ttu-id="7a72b-137">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="7a72b-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="7a72b-138">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7a72b-139">Do pole **Název řešitele** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="7a72b-140">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="7a72b-141">V poli **Komponenty** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="7a72b-142">Každý dílčí komponent musí odkazovat na definici komponenty.</span><span class="sxs-lookup"><span data-stu-id="7a72b-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="7a72b-143">Tento návrh podporuje opakované použití komponent a zajišťuje, že po definování komponenty ji je možné použít v mnoha modelech výrobků.</span><span class="sxs-lookup"><span data-stu-id="7a72b-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="7a72b-144">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-144">Select **Save**.</span></span>
9. <span data-ttu-id="7a72b-145">Vyberte **Podrobnosti řádku kusovníku**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="7a72b-146">Formulář Podrobnosti řádku Kusovníku umožňuje uživatelům vybrat požadované vlastnosti pro dílčí komponentu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="7a72b-147">Všechny vlastnosti mohou mít stanovenou pevnou hodnotu nebo namapovanou hodnotu k atributu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="7a72b-148">Mapování na atribut má za výsledek, že vlastnosti řádku kusovníku získají odlišné hodnoty v závislosti na výběru konfigurace.</span><span class="sxs-lookup"><span data-stu-id="7a72b-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="7a72b-149">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="7a72b-150">Každý dílčí představuje základní konfigurovatelný produkt s technologií konfigurace založenou na omezeních.</span><span class="sxs-lookup"><span data-stu-id="7a72b-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="7a72b-151">Odkaz je vytvořen prostřednictvím čísla položky.</span><span class="sxs-lookup"><span data-stu-id="7a72b-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="7a72b-152">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="7a72b-153">Vyberte možnost **Ano** v poli **Výpočet**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="7a72b-154">Možnost nastavení výpočtu zajišťuje, že výrobek bude zahrnut při spuštění výpočtu nákladů pro produkt.</span><span class="sxs-lookup"><span data-stu-id="7a72b-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="7a72b-155">Vyberte kartu **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="7a72b-156">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="7a72b-157">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="7a72b-158">Pole množství určuje, kolik tohoto produktu bude spotřebováno v konfigurovaném produktu.</span><span class="sxs-lookup"><span data-stu-id="7a72b-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="7a72b-159">Zaškrtněte políčko položky **Nastavit**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="7a72b-160">V poli **Podle sérií** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7a72b-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="7a72b-161">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a72b-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]