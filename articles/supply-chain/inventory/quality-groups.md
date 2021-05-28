---
title: Skupiny kvality položek
description: Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272cb748e0a2722d9744fe6b357d767a1d6aeb26
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022245"
---
# <a name="item-quality-groups"></a><span data-ttu-id="27342-103">Skupiny kvality položek</span><span class="sxs-lookup"><span data-stu-id="27342-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27342-104">Skupina kvality představuje společné požadavky na testování položek.</span><span class="sxs-lookup"><span data-stu-id="27342-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="27342-105">Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="27342-106">K nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce přejděte do **Řízení zásob \> Nastavení \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="27342-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="27342-107">Po určení požadavků na testování na stránce **Testovací skupiny** můžete definovat pravidla pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="27342-108">Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="27342-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="27342-109">Namísto toho můžete na stránce **Přidružení kvality** určít pravidla pro skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="27342-110">Příklad skupiny kvality zboží</span><span class="sxs-lookup"><span data-stu-id="27342-110">Example of an item quality group</span></span>

<span data-ttu-id="27342-111">Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování.</span><span class="sxs-lookup"><span data-stu-id="27342-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="27342-112">Tak společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny.</span><span class="sxs-lookup"><span data-stu-id="27342-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="27342-113">Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování.</span><span class="sxs-lookup"><span data-stu-id="27342-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="27342-114">Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="27342-115">Stejná společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole.</span><span class="sxs-lookup"><span data-stu-id="27342-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="27342-116">Tak společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="27342-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="27342-117">Vytvoření skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="27342-117">Create a quality group</span></span>

<span data-ttu-id="27342-118">Pokud chcete vytvořit skupinu kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="27342-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="27342-119">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="27342-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="27342-120">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="27342-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="27342-121">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="27342-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="27342-122">**Skupina kvality** - Zadejte jedinečné ID nebo název skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="27342-123">**Popis** - Zadejte podrobný popis typu skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="27342-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="27342-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="27342-125">Manuální přidání položek do skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="27342-125">Manually add items to a quality group</span></span>

<span data-ttu-id="27342-126">Chcete-li ručně přidat položky do skupiny kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="27342-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="27342-127">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="27342-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="27342-128">Vyberte skupinu kvality, do které chcete přidat položky.</span><span class="sxs-lookup"><span data-stu-id="27342-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="27342-129">V podokně akcí zvolte **Položky**.</span><span class="sxs-lookup"><span data-stu-id="27342-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="27342-130">Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="27342-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="27342-131">Poté pro nový řádek nastavte pole **Číslo položky** na číslo položky, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="27342-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="27342-132">Opakujte předchozí krok pro každou další položku, kterou je třeba přidat.</span><span class="sxs-lookup"><span data-stu-id="27342-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="27342-133">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="27342-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="27342-134">Přidání více položek do skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="27342-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="27342-135">Chcete-li přidat více položek do skupiny kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="27342-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="27342-136">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="27342-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="27342-137">Vytvořte nebo vyberte skupinu kvality, do které chcete přidat položky.</span><span class="sxs-lookup"><span data-stu-id="27342-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="27342-138">V podokně akcí zvolte **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="27342-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="27342-139">V dialogovém okně **Poptávka** zadejte kritéria filtru pro položky, které chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="27342-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="27342-140">Můžete například filtrovat všechny položky v konkrétní skupině položek.</span><span class="sxs-lookup"><span data-stu-id="27342-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="27342-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="27342-141">Select **OK**.</span></span>
1. <span data-ttu-id="27342-142">V dialogovém okně **Přidání položek** mřížka zobrazuje všechny položky, které odpovídají vašemu dotazu.</span><span class="sxs-lookup"><span data-stu-id="27342-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="27342-143">Zkontrolujte výsledky.</span><span class="sxs-lookup"><span data-stu-id="27342-143">Review the results.</span></span>

    <span data-ttu-id="27342-144">Pokud jsou nutné nějaké změny, vyberte **Vybrat** pro návrat do dialogového okna **Poptávka** a upravte svůj dotaz.</span><span class="sxs-lookup"><span data-stu-id="27342-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="27342-145">Pokud výsledky zahrnují všechny položky, které chcete přidat, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="27342-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="27342-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="27342-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="27342-147">Ručně přidružte položku ke skupině kvality</span><span class="sxs-lookup"><span data-stu-id="27342-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="27342-148">Chcete-li ručně přidružit položku ke skupině kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="27342-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="27342-149">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality položek**.</span><span class="sxs-lookup"><span data-stu-id="27342-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="27342-150">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="27342-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="27342-151">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="27342-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="27342-152">**Číslo položky** - Vyberte číslo položky, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="27342-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="27342-153">**Skupina kvality** - Vyberte skupinu kvality, kterou chcete přiřadit k položce.</span><span class="sxs-lookup"><span data-stu-id="27342-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="27342-154">Opakujte předchozí krok pro každou další kombinaci položky a skupiny kvality, které je třeba přidat.</span><span class="sxs-lookup"><span data-stu-id="27342-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="27342-155">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="27342-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="27342-156">Ručně přidejte skupinu kvality ze stránky Vydané produkty</span><span class="sxs-lookup"><span data-stu-id="27342-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="27342-157">Pro ruční přidání skupiny kvality ze stránky **Vydané produkty** postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="27342-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="27342-158">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="27342-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="27342-159">Vyberte produkt, ke kterému chcete přiřadit skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="27342-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="27342-160">V podokně Akce na kartě **Spravovat sklad** ve skupině **Kvalita** vyberte **Skupiny kvality položek**.</span><span class="sxs-lookup"><span data-stu-id="27342-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="27342-161">Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="27342-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="27342-162">Poté pro nový řádek nastavte pole **Skupina kvality** na skupinu kvality, kterou chcete produktu přiřadit.</span><span class="sxs-lookup"><span data-stu-id="27342-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="27342-163">Opakujte předchozí krok pro každou další skupinu kvality, kterou chcete produktu přiřadit.</span><span class="sxs-lookup"><span data-stu-id="27342-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="27342-164">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="27342-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27342-165">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="27342-165">Additional resources</span></span>

- [<span data-ttu-id="27342-166">Testovací nástroje pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="27342-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="27342-167">Testy správy kvality</span><span class="sxs-lookup"><span data-stu-id="27342-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="27342-168">Testovací skupiny pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="27342-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="27342-169">Testovací proměnné pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="27342-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="27342-170">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="27342-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
