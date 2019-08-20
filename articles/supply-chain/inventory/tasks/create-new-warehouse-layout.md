---
title: Vytvoření nového rozvržení skladu
description: Tento postup popisuje způsob nastavení informací o umístění ve skladu.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f0a52c5d68816a81a94db019387b9ea3ec3efc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845515"
---
# <a name="create-a-new-warehouse-layout"></a><span data-ttu-id="7286e-103">Vytvoření nového rozvržení skladu</span><span class="sxs-lookup"><span data-stu-id="7286e-103">Create a new warehouse layout</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7286e-104">Tento postup popisuje způsob nastavení informací o umístění ve skladu.</span><span class="sxs-lookup"><span data-stu-id="7286e-104">This procedure shows you how to set up information about the locations in a warehouse.</span></span> <span data-ttu-id="7286e-105">To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="7286e-105">This applies only to warehouses created using "basic warehousing" in the Inventory management module, not to warehouses created in the Warehouse management module.</span></span> <span data-ttu-id="7286e-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="7286e-106">You can use this procedure in demo data company USMF, or on your own data.</span></span>


## <a name="set-the-default-location-capacity"></a><span data-ttu-id="7286e-107">Nastavte výchozí kapacitu skladového místa</span><span class="sxs-lookup"><span data-stu-id="7286e-107">Set the default location capacity</span></span>
1. <span data-ttu-id="7286e-108">Přejděte do nabídky Řízení zásob > Nastavení > Parametry řízení zásob a skladu.</span><span class="sxs-lookup"><span data-stu-id="7286e-108">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="7286e-109">Klikněte na kartu Umístění.</span><span class="sxs-lookup"><span data-stu-id="7286e-109">Click the Locations tab.</span></span>
3. <span data-ttu-id="7286e-110">V poli Standardní šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7286e-110">In the Standard width field, enter a number.</span></span>
4. <span data-ttu-id="7286e-111">V poli Standardní hloubka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7286e-111">In the Standard depth field, enter a number.</span></span>
5. <span data-ttu-id="7286e-112">V poli Standardní výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="7286e-112">In the Standard height field, enter a number.</span></span>
6. <span data-ttu-id="7286e-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7286e-113">Click Save.</span></span>
7. <span data-ttu-id="7286e-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7286e-114">Close the page.</span></span>

## <a name="define-the-location-name-format"></a><span data-ttu-id="7286e-115">Definujte formát názvu skladového místa</span><span class="sxs-lookup"><span data-stu-id="7286e-115">Define the location name format</span></span>
1. <span data-ttu-id="7286e-116">Přejděte do části Řízení zásob > Nastavení > Rozdělení zásob > Sklady.</span><span class="sxs-lookup"><span data-stu-id="7286e-116">Go to Inventory management > Setup > Inventory breakdown > Warehouses.</span></span>
2. <span data-ttu-id="7286e-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7286e-117">Click New.</span></span>
3. <span data-ttu-id="7286e-118">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="7286e-118">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="7286e-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="7286e-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7286e-120">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7286e-120">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7286e-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7286e-121">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7286e-122">Přepněte rozšíření oddílu Názvy lokalit.</span><span class="sxs-lookup"><span data-stu-id="7286e-122">Toggle the expansion of the Location names section.</span></span>
    * <span data-ttu-id="7286e-123">Možnosti v tomto oddílu definují výchozí formát pro názvy umístění.</span><span class="sxs-lookup"><span data-stu-id="7286e-123">The options in this section define the default format for location names.</span></span> <span data-ttu-id="7286e-124">V našem příkladu použijeme čísla uličky, stojanu a police.</span><span class="sxs-lookup"><span data-stu-id="7286e-124">In our example, we'll include the aisle number, rack number and shelf number.</span></span>  
8. <span data-ttu-id="7286e-125">Nastavte možnost Včetně uličky na Ano.</span><span class="sxs-lookup"><span data-stu-id="7286e-125">Set the Include aisle option to Yes.</span></span>
9. <span data-ttu-id="7286e-126">Nastavte možnost Včetně stojanu na Ano.</span><span class="sxs-lookup"><span data-stu-id="7286e-126">Set the Include rack option to Yes.</span></span> 
10. <span data-ttu-id="7286e-127">V poli Formát zadejte pro stojan hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7286e-127">In the Format field, for the rack, type a value.</span></span>
    * <span data-ttu-id="7286e-128">Například: -##</span><span class="sxs-lookup"><span data-stu-id="7286e-128">For example: -##</span></span>  
11. <span data-ttu-id="7286e-129">Nastavte možnost Včetně police na Ano.</span><span class="sxs-lookup"><span data-stu-id="7286e-129">Set the Include shelf option to Yes.</span></span>
12. <span data-ttu-id="7286e-130">V poli Formát zadejte pro polici hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7286e-130">In the Format field, for the shelf, type a value.</span></span>
    * <span data-ttu-id="7286e-131">Například: -##</span><span class="sxs-lookup"><span data-stu-id="7286e-131">For example: -##</span></span>  

## <a name="define-warehouse-locations"></a><span data-ttu-id="7286e-132">Definujte umístění ve skladu</span><span class="sxs-lookup"><span data-stu-id="7286e-132">Define warehouse locations</span></span>
1. <span data-ttu-id="7286e-133">V podokně akcí klikněte na možnost Sklad.</span><span class="sxs-lookup"><span data-stu-id="7286e-133">On the Action Pane, click Warehouse.</span></span>
2. <span data-ttu-id="7286e-134">Klikněte na Průvodce skladovým místem.</span><span class="sxs-lookup"><span data-stu-id="7286e-134">Click Location Wizard.</span></span>
3. <span data-ttu-id="7286e-135">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-135">Click Next.</span></span>
4. <span data-ttu-id="7286e-136">Zrušte výběr možnosti Výstupní překladiště</span><span class="sxs-lookup"><span data-stu-id="7286e-136">De-select the Outbound docks option</span></span>
5. <span data-ttu-id="7286e-137">Zrušte výběr možnosti Hromadné umístění</span><span class="sxs-lookup"><span data-stu-id="7286e-137">De-select the Bulk locations option</span></span>
6. <span data-ttu-id="7286e-138">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-138">Click Next.</span></span>
7. <span data-ttu-id="7286e-139">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-139">Click Next.</span></span>
8. <span data-ttu-id="7286e-140">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-140">Click Next.</span></span>
9. <span data-ttu-id="7286e-141">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-141">Click Next.</span></span>
10. <span data-ttu-id="7286e-142">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-142">Click Next.</span></span>
11. <span data-ttu-id="7286e-143">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-143">Click Next.</span></span>
12. <span data-ttu-id="7286e-144">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-144">Click Next.</span></span>
    * <span data-ttu-id="7286e-145">Všimněte si, že zobrazené fyzické dimenze na této stránce jsou ty, které jste nastavili na začátku tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="7286e-145">Note that the physical dimensions shown on this page are the ones that you set at the start of this procedure.</span></span>  
13. <span data-ttu-id="7286e-146">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="7286e-146">Click Next.</span></span>
14. <span data-ttu-id="7286e-147">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="7286e-147">Click Finish.</span></span>
15. <span data-ttu-id="7286e-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="7286e-148">Close the page.</span></span>
16. <span data-ttu-id="7286e-149">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="7286e-149">Refresh the page.</span></span>

