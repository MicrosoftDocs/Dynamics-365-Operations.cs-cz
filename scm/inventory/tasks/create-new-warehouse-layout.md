---
title: "Vytvoření nového rozvržení skladu"
description: "Tento postup popisuje způsob nastavení informací o umístění ve skladu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 253440d81edd6f71b52ae349398e3c6a895bf05c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/12/2017

---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="a49b9-103">Vytvoření nového rozvržení skladu</span><span class="sxs-lookup"><span data-stu-id="a49b9-103">Create a new warehouse layout</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a49b9-104">Tento postup popisuje způsob nastavení informací o umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="a49b9-105">To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="a49b9-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="a49b9-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="a49b9-107">Nastavte výchozí kapacitu skladového místa</span><span class="sxs-lookup"><span data-stu-id="a49b9-107">Set the default location capacity</span></span>
1. <span data-ttu-id="a49b9-108">Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="a49b9-109">Klikněte na kartu Umístění.</span><span class="sxs-lookup"><span data-stu-id="a49b9-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="a49b9-110">V poli Standardní šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="a49b9-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="a49b9-111">V poli Standardní hloubka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="a49b9-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="a49b9-112">V poli Standardní výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="a49b9-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="a49b9-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="a49b9-113">Click Save.</span></span>
7. <span data-ttu-id="a49b9-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a49b9-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="a49b9-115">Definujte formát názvu skladového místa</span><span class="sxs-lookup"><span data-stu-id="a49b9-115">Define the location name format</span></span>
1. <span data-ttu-id="a49b9-116">Přejděte do části Řízení zásob > Nastavení > Rozdělení zásob > Sklady.</span><span class="sxs-lookup"><span data-stu-id="a49b9-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="a49b9-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="a49b9-117">Click New.</span></span>
3. <span data-ttu-id="a49b9-118">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="a49b9-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="a49b9-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="a49b9-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a49b9-120">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="a49b9-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a49b9-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a49b9-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a49b9-122">Přepněte rozšíření oddílu Názvy lokalit.</span><span class="sxs-lookup"><span data-stu-id="a49b9-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="a49b9-123">Možnosti v tomto oddílu definují výchozí formát pro názvy umístění.</span><span class="sxs-lookup"><span data-stu-id="a49b9-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="a49b9-124">V našem příkladu použijeme čísla uličky, stojanu a police.</span><span class="sxs-lookup"><span data-stu-id="a49b9-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="a49b9-125">Nastavte možnost Včetně uličky na Ano.</span><span class="sxs-lookup"><span data-stu-id="a49b9-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="a49b9-126">Nastavte možnost Včetně stojanu na Ano.</span><span class="sxs-lookup"><span data-stu-id="a49b9-126">Set the Include rack option to Yes.</span></span>
10. <span data-ttu-id="a49b9-127">V poli Formát zadejte pro stojan hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="a49b9-128">Například: -##</span><span class="sxs-lookup"><span data-stu-id="a49b9-128">For example: -##</span></span>  
11. <span data-ttu-id="a49b9-129">Nastavte možnost Včetně police na Ano.</span><span class="sxs-lookup"><span data-stu-id="a49b9-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="a49b9-130">V poli Formát zadejte pro polici hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="a49b9-131">Například: -##</span><span class="sxs-lookup"><span data-stu-id="a49b9-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="a49b9-132">Definujte umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="a49b9-132">Define warehouse locations</span></span>
1. <span data-ttu-id="a49b9-133">V podokně akcí klikněte na možnost Sklad.</span><span class="sxs-lookup"><span data-stu-id="a49b9-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="a49b9-134">Klikněte na Průvodce skladovým místem.</span><span class="sxs-lookup"><span data-stu-id="a49b9-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="a49b9-135">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-135">Click Next.</span></span>
4. <span data-ttu-id="a49b9-136">Zrušte výběr možnosti Výstupní překladiště</span><span class="sxs-lookup"><span data-stu-id="a49b9-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="a49b9-137">Zrušte výběr možnosti Hromadné umístění</span><span class="sxs-lookup"><span data-stu-id="a49b9-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="a49b9-138">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-138">Click Next.</span></span>
7. <span data-ttu-id="a49b9-139">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-139">Click Next.</span></span>
8. <span data-ttu-id="a49b9-140">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-140">Click Next.</span></span>
9. <span data-ttu-id="a49b9-141">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-141">Click Next.</span></span>
10. <span data-ttu-id="a49b9-142">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-142">Click Next.</span></span>
11. <span data-ttu-id="a49b9-143">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-143">Click Next.</span></span>
12. <span data-ttu-id="a49b9-144">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-144">Click Next.</span></span>
    * <span data-ttu-id="a49b9-145">Všimněte si, že zobrazené fyzické dimenze na této stránce jsou ty, které jste nastavili na začátku tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="a49b9-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="a49b9-146">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="a49b9-146">Click Next.</span></span>
14. <span data-ttu-id="a49b9-147">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="a49b9-147">Click Finish.</span></span>
15. <span data-ttu-id="a49b9-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="a49b9-148">Close the page.</span></span>
16. <span data-ttu-id="a49b9-149">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="a49b9-149">Refresh the page.</span></span>

