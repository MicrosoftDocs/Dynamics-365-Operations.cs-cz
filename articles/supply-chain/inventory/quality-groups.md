---
title: Skupiny kvality položek
description: Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 3074a6a8cc054be045bf593b509e76a1043af0b7
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956575"
---
# <a name="item-quality-groups"></a><span data-ttu-id="811e3-103">Skupiny kvality položek</span><span class="sxs-lookup"><span data-stu-id="811e3-103">Item quality groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="811e3-104">Skupina kvality představuje společné požadavky na testování položek.</span><span class="sxs-lookup"><span data-stu-id="811e3-104">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="811e3-105">Toto téma popisuje, jak použít a vytvořit skupiny kvality položek k logickému seskupení produktů tak, aby je bylo možné přiřadit k asociacím kvality pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-105">This topic describes how to use and create item quality groups to logically group products so that they can be assigned to quality associations for the automatic generation of quality orders.</span></span>

<span data-ttu-id="811e3-106">K nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce přejděte do **Řízení zásob \> Nastavení \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="811e3-106">To set up, edit, and view the items that are assigned to a quality group, or the quality groups that are assigned to an item, go to **Inventory management \> Setup \> Quality groups**.</span></span> <span data-ttu-id="811e3-107">Po určení požadavků na testování na stránce **Testovací skupiny** můžete definovat pravidla pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-107">After you define the test requirements on the **Test groups** page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="811e3-108">Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="811e3-108">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="811e3-109">Namísto toho můžete na stránce **Přidružení kvality** určít pravidla pro skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-109">Instead, you can define the rules for a quality group on the **Quality associations** page.</span></span>

## <a name="example-of-an-item-quality-group"></a><span data-ttu-id="811e3-110">Příklad skupiny kvality zboží</span><span class="sxs-lookup"><span data-stu-id="811e3-110">Example of an item quality group</span></span>

<span data-ttu-id="811e3-111">Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování.</span><span class="sxs-lookup"><span data-stu-id="811e3-111">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="811e3-112">Tak společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny.</span><span class="sxs-lookup"><span data-stu-id="811e3-112">Therefore, the company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="811e3-113">Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování.</span><span class="sxs-lookup"><span data-stu-id="811e3-113">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="811e3-114">Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-114">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span>

<span data-ttu-id="811e3-115">Stejná společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole.</span><span class="sxs-lookup"><span data-stu-id="811e3-115">The same company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="811e3-116">Tak společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="811e3-116">Therefore, the company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="811e3-117">Vytvoření skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-117">Create a quality group</span></span>

<span data-ttu-id="811e3-118">Pokud chcete vytvořit skupinu kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811e3-118">To create a quality group, follow these steps.</span></span>

1. <span data-ttu-id="811e3-119">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="811e3-119">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="811e3-120">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="811e3-120">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="811e3-121">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="811e3-121">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="811e3-122">**Skupina kvality** - Zadejte jedinečné ID nebo název skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-122">**Quality group** – Enter a unique ID or name for the quality group.</span></span>
    - <span data-ttu-id="811e3-123">**Popis** - Zadejte podrobný popis typu skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-123">**Description** – Enter a detailed description of the quality group.</span></span>

1. <span data-ttu-id="811e3-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="811e3-124">Close the page.</span></span>

## <a name="manually-add-items-to-a-quality-group"></a><span data-ttu-id="811e3-125">Manuální přidání položek do skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-125">Manually add items to a quality group</span></span>

<span data-ttu-id="811e3-126">Chcete-li ručně přidat položky do skupiny kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811e3-126">To manually add items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="811e3-127">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="811e3-127">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="811e3-128">Vyberte skupinu kvality, do které chcete přidat položky.</span><span class="sxs-lookup"><span data-stu-id="811e3-128">Select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="811e3-129">V podokně akcí zvolte **Položky**.</span><span class="sxs-lookup"><span data-stu-id="811e3-129">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="811e3-130">Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="811e3-130">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="811e3-131">Poté pro nový řádek nastavte pole **Číslo položky** na číslo položky, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="811e3-131">Then, for the new row, set the **Item number** field to the item number that you want to add.</span></span>
1. <span data-ttu-id="811e3-132">Opakujte předchozí krok pro každou další položku, kterou je třeba přidat.</span><span class="sxs-lookup"><span data-stu-id="811e3-132">Repeat the previous step for each additional item that must be added.</span></span>
1. <span data-ttu-id="811e3-133">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="811e3-133">Close the pages.</span></span>

## <a name="add-multiple-items-to-a-quality-group"></a><span data-ttu-id="811e3-134">Přidání více položek do skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-134">Add multiple items to a quality group</span></span>

<span data-ttu-id="811e3-135">Chcete-li přidat více položek do skupiny kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811e3-135">To add multiple items to a quality group, follow these steps.</span></span>

1. <span data-ttu-id="811e3-136">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="811e3-136">Go to **Inventory management \> Setup \> Quality control \> Quality groups**.</span></span>
1. <span data-ttu-id="811e3-137">Vytvořte nebo vyberte skupinu kvality, do které chcete přidat položky.</span><span class="sxs-lookup"><span data-stu-id="811e3-137">Create or select the quality group that you want to add items to.</span></span>
1. <span data-ttu-id="811e3-138">V podokně akcí zvolte **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="811e3-138">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="811e3-139">V dialogovém okně **Poptávka** zadejte kritéria filtru pro položky, které chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="811e3-139">In the **Inquiry** dialog box, enter the filter criteria for the items that you want to add.</span></span> <span data-ttu-id="811e3-140">Můžete například filtrovat všechny položky v konkrétní skupině položek.</span><span class="sxs-lookup"><span data-stu-id="811e3-140">For example, you might filter for all items in a specific item group.</span></span>
1. <span data-ttu-id="811e3-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="811e3-141">Select **OK**.</span></span>
1. <span data-ttu-id="811e3-142">V dialogovém okně **Přidání položek** mřížka zobrazuje všechny položky, které odpovídají vašemu dotazu.</span><span class="sxs-lookup"><span data-stu-id="811e3-142">In the **Add items** dialog box, a grid shows all the items that match your query.</span></span> <span data-ttu-id="811e3-143">Zkontrolujte výsledky.</span><span class="sxs-lookup"><span data-stu-id="811e3-143">Review the results.</span></span>

    <span data-ttu-id="811e3-144">Pokud jsou nutné nějaké změny, vyberte **Vybrat** pro návrat do dialogového okna **Poptávka** a upravte svůj dotaz.</span><span class="sxs-lookup"><span data-stu-id="811e3-144">If any changes are required, select **Select** to return to the **Inquiry** dialog box, and adjust your query.</span></span>

1. <span data-ttu-id="811e3-145">Pokud výsledky zahrnují všechny položky, které chcete přidat, vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="811e3-145">When the results include all the items that you want to add, select **OK**.</span></span>
1. <span data-ttu-id="811e3-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="811e3-146">Close the page.</span></span>

## <a name="manually-associate-an-item-with-a-quality-group"></a><span data-ttu-id="811e3-147">Ručně přidružte položku ke skupině kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-147">Manually associate an item with a quality group</span></span>

<span data-ttu-id="811e3-148">Chcete-li ručně přidružit položku ke skupině kvality, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811e3-148">To manually associate an item with a quality group, follow these steps.</span></span>

1. <span data-ttu-id="811e3-149">Přejděte na **Řízení zásob \> Nastavení \> Řízení kvality \> Skupiny kvality položek**.</span><span class="sxs-lookup"><span data-stu-id="811e3-149">Go to **Inventory management \> Setup \> Quality control \> Item quality groups**.</span></span>
1. <span data-ttu-id="811e3-150">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="811e3-150">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="811e3-151">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="811e3-151">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="811e3-152">**Číslo položky** - Vyberte číslo položky, kterou chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="811e3-152">**Item number** – Select the item number to add.</span></span>
    - <span data-ttu-id="811e3-153">**Skupina kvality** - Vyberte skupinu kvality, kterou chcete přiřadit k položce.</span><span class="sxs-lookup"><span data-stu-id="811e3-153">**Quality group** – Select the quality group to assign to the item.</span></span>

1. <span data-ttu-id="811e3-154">Opakujte předchozí krok pro každou další kombinaci položky a skupiny kvality, které je třeba přidat.</span><span class="sxs-lookup"><span data-stu-id="811e3-154">Repeat the previous step for each additional combination of an item and a quality group that must be added.</span></span>
1. <span data-ttu-id="811e3-155">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="811e3-155">Close the pages.</span></span>

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a><span data-ttu-id="811e3-156">Ručně přidejte skupinu kvality ze stránky Vydané produkty</span><span class="sxs-lookup"><span data-stu-id="811e3-156">Manually add a quality group from the Released products page</span></span>

<span data-ttu-id="811e3-157">Pro ruční přidání skupiny kvality ze stránky **Vydané produkty** postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="811e3-157">To manually add a quality group from the **Released products** page, follow these steps.</span></span>

1. <span data-ttu-id="811e3-158">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="811e3-158">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="811e3-159">Vyberte produkt, ke kterému chcete přiřadit skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="811e3-159">Select the product that you want to assign a quality group to.</span></span>
1. <span data-ttu-id="811e3-160">V podokně Akce na kartě **Spravovat sklad** ve skupině **Kvalita** vyberte **Skupiny kvality položek**.</span><span class="sxs-lookup"><span data-stu-id="811e3-160">On the Action Pane, on the **Manage inventory** tab, in the **Quality** group, select **Item quality groups**.</span></span>
1. <span data-ttu-id="811e3-161">Na stránce **Položky ve skupinách kvality** v podokně akcí vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="811e3-161">On the **Items in quality groups** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="811e3-162">Poté pro nový řádek nastavte pole **Skupina kvality** na skupinu kvality, kterou chcete produktu přiřadit.</span><span class="sxs-lookup"><span data-stu-id="811e3-162">Then, for the new row, set the **Quality group** field to the quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="811e3-163">Opakujte předchozí krok pro každou další skupinu kvality, kterou chcete produktu přiřadit.</span><span class="sxs-lookup"><span data-stu-id="811e3-163">Repeat the previous step for each additional quality group that you want to assign to the product.</span></span>
1. <span data-ttu-id="811e3-164">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="811e3-164">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="811e3-165">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="811e3-165">Additional resources</span></span>

- [<span data-ttu-id="811e3-166">Testovací nástroje pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-166">Quality management test instruments</span></span>](quality-test-instruments.md)
- [<span data-ttu-id="811e3-167">Testy správy kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-167">Quality management tests</span></span>](quality-tests.md)
- [<span data-ttu-id="811e3-168">Testovací skupiny pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-168">Quality management test groups</span></span>](quality-test-groups.md)
- [<span data-ttu-id="811e3-169">Testovací proměnné pro řízení kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-169">Quality management test variables</span></span>](quality-test-variables.md)
- [<span data-ttu-id="811e3-170">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="811e3-170">Quality associations</span></span>](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
