--- 
title: "Nastavení položky nabídky na mobilním zařízení pro dokončení práce v nákupní objednávce"
description: "Tento postup popisuje způsob nastavení položky nabídky Mobilní zařízení."
author: ShylaThompson
manager: AnnBe
ms.date: 08/25/2016
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
ms.openlocfilehash: 31007031b761cfed6b5a97ebb829be4d200bc82d
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-a-mobile-device-menu-item-for-completing-work-in-a-purchase-order"></a><span data-ttu-id="943c6-103">Nastavení položky nabídky na mobilním zařízení pro dokončení práce v nákupní objednávce</span><span class="sxs-lookup"><span data-stu-id="943c6-103">Set up a mobile device menu item for completing work in a purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="943c6-104">Tento postup popisuje způsob nastavení položky nabídky Mobilní zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-104">This procedure shows how to set up a Mobile device menu item.</span></span> <span data-ttu-id="943c6-105">V tomto příkladu slouží tato položka nabídky k provedení práce typu Nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="943c6-105">In this example, the menu item is used for performing work of type Purchase order.</span></span> <span data-ttu-id="943c6-106">Platná práce je určena pracovní třídou, která je přiřazena k položce nabídky.</span><span class="sxs-lookup"><span data-stu-id="943c6-106">The work class that’s associated with the menu item determines which work is valid.</span></span> <span data-ttu-id="943c6-107">Tohoto průvodce můžete použít s ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="943c6-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="943c6-108">Tento proces obvykle provádí správce skladu.</span><span class="sxs-lookup"><span data-stu-id="943c6-108">This procedure is typically carried out by a warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="943c6-109">Vytvoření položky nabídky mobilních zařízení</span><span class="sxs-lookup"><span data-stu-id="943c6-109">Create a mobile device menu item</span></span>
1. <span data-ttu-id="943c6-110">Přejděte do položek nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-110">Go to Mobile device menu items.</span></span>
2. <span data-ttu-id="943c6-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="943c6-111">Click New.</span></span>
3. <span data-ttu-id="943c6-112">Do pole Položky nabídky mobilního zařízení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="943c6-112">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="943c6-113">Zadejte jedinečnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="943c6-113">Enter a unique value.</span></span> <span data-ttu-id="943c6-114">Můžete například zadat „Přesun nákupní objednávky“.</span><span class="sxs-lookup"><span data-stu-id="943c6-114">For example, you could type POMove.</span></span> <span data-ttu-id="943c6-115">Zapamatujte si hodnotu – budete ji potřebovat později.</span><span class="sxs-lookup"><span data-stu-id="943c6-115">Remember the value, you'll need it later.</span></span>  
4. <span data-ttu-id="943c6-116">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="943c6-116">In the Title field, type a value.</span></span>
    * <span data-ttu-id="943c6-117">Toto je název, který se zobrazí na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-117">This is the title which will be displayed on the mobile device.</span></span> <span data-ttu-id="943c6-118">Můžete například zadat „Přesun nákupní objednávky“.</span><span class="sxs-lookup"><span data-stu-id="943c6-118">For example, you could type PO Move.</span></span>  
5. <span data-ttu-id="943c6-119">V poli Režim vyberte „Práce“.</span><span class="sxs-lookup"><span data-stu-id="943c6-119">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="943c6-120">Vyberte možnost Ano v poli Použít stávající práci.</span><span class="sxs-lookup"><span data-stu-id="943c6-120">Select Yes in the Use existing work field.</span></span>
    * <span data-ttu-id="943c6-121">Tato položka nabídky v mobilním zařízení se používá k provedení stávající práce.</span><span class="sxs-lookup"><span data-stu-id="943c6-121">This mobile device menu item is used to perform existing work.</span></span> <span data-ttu-id="943c6-122">Proto je nutné nastavit tuto hodnotu na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="943c6-122">Therefore you must set this value to Yes.</span></span>  
    * <span data-ttu-id="943c6-123">Pole Zobrazit stav zásob určuje, zda se stav zásob na skladě zobrazí pracovníkovi skladu na mobilním zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-123">The Display inventory status field determines whether the inventory status of the on-hand inventory will be displayed to the warehouse worker on the mobile device.</span></span>  
7. <span data-ttu-id="943c6-124">V poli „Řídí“ vyberte „Systémovém seskupení“.</span><span class="sxs-lookup"><span data-stu-id="943c6-124">In the Directed by field, select 'System grouping'.</span></span>
    * <span data-ttu-id="943c6-125">Pokud vyberete jinou možnost v poli Řídí, v části Obecné na této stránce se zobrazí další pole.</span><span class="sxs-lookup"><span data-stu-id="943c6-125">When you select something in the Directed by field, additional fields appear in the General section on this page.</span></span> <span data-ttu-id="943c6-126">Zobrazená pole závisí na vašem výběru.</span><span class="sxs-lookup"><span data-stu-id="943c6-126">The fields that appear depend on what you selected.</span></span> <span data-ttu-id="943c6-127">Při výběru možnosti Systémové seskupení budou přidána dvě nová pole.</span><span class="sxs-lookup"><span data-stu-id="943c6-127">When you select System grouping, two new fields are added.</span></span> <span data-ttu-id="943c6-128">Ty jsou vysvětleny níže.</span><span class="sxs-lookup"><span data-stu-id="943c6-128">These are explained below.</span></span>  
8. <span data-ttu-id="943c6-129">V poli Systémové seskupení vyberte WorkPoolId.</span><span class="sxs-lookup"><span data-stu-id="943c6-129">In the System grouping field, select 'WorkPoolId'.</span></span>
    * <span data-ttu-id="943c6-130">Když pracovníci skladu otevřou tuto položku nabídky, budou vyzváni ke kontrole ID fondu práce.</span><span class="sxs-lookup"><span data-stu-id="943c6-130">When warehouse workers open this menu item, they’ll be asked to scan a Work pool ID.</span></span> <span data-ttu-id="943c6-131">Uživateli budou předloženy všechny pracovní objednávky s tímto ID fondu práce a otevřené řádky pracovního příkazu, do kterých byla k této položce nabídky přidána některá z pracovních tříd.</span><span class="sxs-lookup"><span data-stu-id="943c6-131">All work orders with this Work pool ID and open work order lines with one of the work classes added to this menu item will be pushed to the user.</span></span>  
9. <span data-ttu-id="943c6-132">Zadejte hodnotu do pole Popisek systémového seskupení.</span><span class="sxs-lookup"><span data-stu-id="943c6-132">In the System grouping label field, type a value.</span></span>
    * <span data-ttu-id="943c6-133">Tento textový popisek se zobrazí uživateli mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-133">This is the text displayed to the user on the mobile device.</span></span> <span data-ttu-id="943c6-134">Můžete například zadat „Fond práce“.</span><span class="sxs-lookup"><span data-stu-id="943c6-134">For example, you could type Work pool.</span></span>  
10. <span data-ttu-id="943c6-135">Vyberte možnost Ano v poli Přepsat registrační značku během vložení.</span><span class="sxs-lookup"><span data-stu-id="943c6-135">Select Yes in the Override license plate during put field.</span></span>
    * <span data-ttu-id="943c6-136">Tato možnost umožňuje pracovníkům skladu přepsat cílové registrační značky, když jsou položky odloženy do umístění řízeného registračními značkami.</span><span class="sxs-lookup"><span data-stu-id="943c6-136">This option allows warehouse workers to override the target license plate when items are put down on a license plate controlled location.</span></span>  
11. <span data-ttu-id="943c6-137">Vyberte možnost Ano v poli Odložená skupina.</span><span class="sxs-lookup"><span data-stu-id="943c6-137">Select Yes in the Group put away field.</span></span>
    * <span data-ttu-id="943c6-138">Pokud všechny řádky vložení v pracovní objednávce sdílí stejné umístění, uživatel obdrží jednu kombinovanou instrukci pro vložení pro všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="943c6-138">If all the Put lines on the work order share the same location, the user will receive one combined Put instruction for all lines.</span></span>  
    * <span data-ttu-id="943c6-139">ID šablony auditu: šablona auditu práce umožňuje určit, zda je třeba pracovní proces pro položku nabídky přerušit, aby mohla být provedena jiná operace.</span><span class="sxs-lookup"><span data-stu-id="943c6-139">Audit template ID: A work audit template allows you to specify that the work process for a menu item should be interrupted so that another operation can be performed.</span></span> <span data-ttu-id="943c6-140">Pokud je tedy například tato položka nabídky určena pro vstupní práci, šablona auditu může vyžadovat, aby pracovník ověřil teplotu.</span><span class="sxs-lookup"><span data-stu-id="943c6-140">For example, if this menu item is for inbound work, the audit template might require that the worker checks the temperature.</span></span> <span data-ttu-id="943c6-141">Bod, ve kterém bude proces přerušen, je určen v šabloně auditu, a může se například jednat o zahájení nebo dokončení práce, nebo o okamžik, kdy dojde ke změně stavu.</span><span class="sxs-lookup"><span data-stu-id="943c6-141">The point at which the process is interrupted is specified on the audit template and can be, for example, when work is started or completed, or when its status changes.</span></span>  
12. <span data-ttu-id="943c6-142">Rozbalte sekci Pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="943c6-142">Expand the Work classes section.</span></span>
13. <span data-ttu-id="943c6-143">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="943c6-143">Click New.</span></span>
14. <span data-ttu-id="943c6-144">Zadejte „Nákup“ do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="943c6-144">In the Work class ID field, type 'Purchase'.</span></span>
    * <span data-ttu-id="943c6-145">Pracovní fond omezuje práci, pro kterou lze používat položku nabídky.</span><span class="sxs-lookup"><span data-stu-id="943c6-145">The work pool restricts the work that the menu item can be used for.</span></span> <span data-ttu-id="943c6-146">V tomto případě se použije pro otevřené řádky pracovního příkazu, které mají ID třídy pro práci u nákupu.</span><span class="sxs-lookup"><span data-stu-id="943c6-146">In this case it will be used for open work order lines that have the Purchase work class ID.</span></span>  
15. <span data-ttu-id="943c6-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="943c6-147">Click Save.</span></span>

## <a name="set-up-work-confirmation"></a><span data-ttu-id="943c6-148">Potvrzení nastavení práce</span><span class="sxs-lookup"><span data-stu-id="943c6-148">Set up work confirmation</span></span>
1. <span data-ttu-id="943c6-149">Klepněte na Nastavení potvrzení práce.</span><span class="sxs-lookup"><span data-stu-id="943c6-149">Click Work confirmation setup.</span></span>
2. <span data-ttu-id="943c6-150">V poli Typ práce vyberte „Vybrat“.</span><span class="sxs-lookup"><span data-stu-id="943c6-150">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="943c6-151">Zaškrtněte políčko Potvrdit automaticky.</span><span class="sxs-lookup"><span data-stu-id="943c6-151">Select the Auto confirm check box.</span></span>
    * <span data-ttu-id="943c6-152">Pracovní instrukce s typem práce „vyskladnění“ bude automaticky potvrzena.</span><span class="sxs-lookup"><span data-stu-id="943c6-152">The work instruction with work type Pick will be auto-confirmed.</span></span> <span data-ttu-id="943c6-153">Tento pokyn není prezentován uživateli.</span><span class="sxs-lookup"><span data-stu-id="943c6-153">This instruction will not be presented to the user.</span></span>  
4. <span data-ttu-id="943c6-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="943c6-154">Click New.</span></span>
5. <span data-ttu-id="943c6-155">V poli Typ práce vyberte „Vložit“.</span><span class="sxs-lookup"><span data-stu-id="943c6-155">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="943c6-156">Zaškrtněte políčko Potvrzení umístění.</span><span class="sxs-lookup"><span data-stu-id="943c6-156">Select the Location confirmation check box.</span></span>
    * <span data-ttu-id="943c6-157">Pracovník skladu, bude požádán, aby provedl kontrolní skenování v umístění, ve kterém je zboží odloženo.</span><span class="sxs-lookup"><span data-stu-id="943c6-157">The warehouse worker will be asked to perform a confirmation scan of the location, when the item is put down.</span></span>  
7. <span data-ttu-id="943c6-158">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="943c6-158">Click Save.</span></span>
8. <span data-ttu-id="943c6-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="943c6-159">Close the page.</span></span>
9. <span data-ttu-id="943c6-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="943c6-160">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="943c6-161">Přidání položky nabídky do nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="943c6-161">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="943c6-162">Přejděte do nabídky Mobilní zařízení.</span><span class="sxs-lookup"><span data-stu-id="943c6-162">Go to Mobile device menu.</span></span>
2. <span data-ttu-id="943c6-163">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="943c6-163">Click Edit.</span></span>
3. <span data-ttu-id="943c6-164">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="943c6-164">Use the Quick Filter to find records.</span></span> <span data-ttu-id="943c6-165">Můžete například filtrovat v poli Jméno pomocí hodnoty „inbound“.</span><span class="sxs-lookup"><span data-stu-id="943c6-165">For example, filter on the Name field with a value of 'inbound'.</span></span>
    * <span data-ttu-id="943c6-166">Chcete najít nabídku, kterou lze použít pro vstupní položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="943c6-166">You want to find the menu you use for inbound menu items.</span></span> <span data-ttu-id="943c6-167">V USMF se tato položka nazývá Příchozí.</span><span class="sxs-lookup"><span data-stu-id="943c6-167">In USMF this is called Inbound.</span></span>  
4. <span data-ttu-id="943c6-168">Ve stromu vyberte „hodnotu“.</span><span class="sxs-lookup"><span data-stu-id="943c6-168">In the tree, select 'a value'.</span></span>
5. <span data-ttu-id="943c6-169">Klepněte na šipku ukazující napravo.</span><span class="sxs-lookup"><span data-stu-id="943c6-169">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="943c6-170">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="943c6-170">Click Save.</span></span>
7. <span data-ttu-id="943c6-171">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="943c6-171">Close the page.</span></span>


