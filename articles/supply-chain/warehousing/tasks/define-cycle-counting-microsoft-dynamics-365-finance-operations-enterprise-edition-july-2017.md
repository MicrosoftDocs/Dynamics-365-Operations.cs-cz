---
title: 'Definování cyklické inventury '
description: Cyklická inventura je skladový proces, který slouží k auditu skladových položek na skladě.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountThreshold, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSParameters, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1424bc4c4ff0f8528d6577e80324082cb2ec7f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977155"
---
# <a name="define-cycle-counting"></a><span data-ttu-id="83592-103">Definování cyklické inventury </span><span class="sxs-lookup"><span data-stu-id="83592-103">Define cycle counting</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="83592-104">Cyklická inventura je skladový proces, který slouží k auditu skladových položek na skladě.</span><span class="sxs-lookup"><span data-stu-id="83592-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="83592-105">Toto zaznamenávání úkolu zobrazuje způsob, jak na to: nastavte výchozí prioritu inventury; povolte položku nabídky mobilního zařízení, aby zpracovávala operace výdeje i výpočtu; povolte prahovou hodnotu spuštění inventury když skladové místo bude prázdné; povolte plán cyklické inventury pro konkrétní položku v určitém skladu.</span><span class="sxs-lookup"><span data-stu-id="83592-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="83592-106">Obvykle jsou tyto úlohy prováděny vedoucím skladu.</span><span class="sxs-lookup"><span data-stu-id="83592-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="83592-107">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="83592-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="83592-108">Nastavení priority inventury</span><span class="sxs-lookup"><span data-stu-id="83592-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="83592-109">V **navigačním podokně** přejděte na **Moduly > Řízení skladu > Nastavení > Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="83592-109">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="83592-110">Klikněte na kartu **Cyklická inventura**.</span><span class="sxs-lookup"><span data-stu-id="83592-110">Click the **Cycle counting** tab.</span></span>
3. <span data-ttu-id="83592-111">V poli **Výchozí pracovní priorita pro cyklickou inventuru** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="83592-111">In the **Default cycle count work priority** field, enter a number.</span></span> <span data-ttu-id="83592-112">Tento krok změní prioritu práce cyklické inventury ve srovnání s jinými typy práce ve skladu.</span><span class="sxs-lookup"><span data-stu-id="83592-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="83592-113">Zadáním čísla, které je nižší, než je číslo pro jiné typy prací, můžete zvýšit prioritu práce cyklické inventury.</span><span class="sxs-lookup"><span data-stu-id="83592-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="83592-114">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-114">Click **Save**.</span></span>
5. <span data-ttu-id="83592-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83592-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="83592-116">Povolení mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="83592-116">Enable the mobile device</span></span>
1. <span data-ttu-id="83592-117">V **navigačním podokně** přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="83592-117">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="83592-118">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-118">Click **New**.</span></span>
3. <span data-ttu-id="83592-119">Do pole **Název položky nabídky** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="83592-119">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="83592-120">Zadejte hodnotu do pole **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="83592-120">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="83592-121">V poli **Režim** vyberte „Práce“.</span><span class="sxs-lookup"><span data-stu-id="83592-121">In the **Mode** field, select 'Work'.</span></span>
6. <span data-ttu-id="83592-122">Nastavte hodnotu možnosti **Použít stávající práci** na Ano.</span><span class="sxs-lookup"><span data-stu-id="83592-122">Set the **Use existing work** option to Yes.</span></span> <span data-ttu-id="83592-123">Pokud vyberete volbu Ano, systém bude hledat existující práci, když je použita položka nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="83592-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="83592-124">V poli **Řídí** vyberte „Řízeno systémem“.</span><span class="sxs-lookup"><span data-stu-id="83592-124">In the **Directed by** field, select 'System directed'.</span></span> <span data-ttu-id="83592-125">Pokud je vybráno Řízeno systémem, pracovník skladu bude přesměrován na otevřenou práci v definovaných pracovních třídách.</span><span class="sxs-lookup"><span data-stu-id="83592-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="83592-126">(Tyto pracovní třídy vytvoříme příště.)</span><span class="sxs-lookup"><span data-stu-id="83592-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="83592-127">Rozbalte záložku s náhledem **Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="83592-127">Expand the **Work classes** fastTab.</span></span> <span data-ttu-id="83592-128">Dále vytvoříme dvě pracovní třídy pro použití s touto položkou nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="83592-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="83592-129">Při použití položky nabídky budou dotazovány tyto pracovní třídy, a ve výsledku bude uživateli zobrazena práce s nejvyšší prioritou.</span><span class="sxs-lookup"><span data-stu-id="83592-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="83592-130">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-130">Click **New**.</span></span>
10. <span data-ttu-id="83592-131">Vyberte hodnotu v poli **ID pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="83592-131">In the **Work class ID** field, select a value.</span></span>
11. <span data-ttu-id="83592-132">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-132">Click **New**.</span></span>
12. <span data-ttu-id="83592-133">Vyberte hodnotu v poli **ID pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="83592-133">In the **Work class ID** field, select a value.</span></span>
13. <span data-ttu-id="83592-134">V **podokně akcí** klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-134">In the **Action Pane**, click **Save**.</span></span>
14. <span data-ttu-id="83592-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83592-135">Close the page.</span></span>
15. <span data-ttu-id="83592-136">V **navigačním podokně** přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="83592-136">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
16. <span data-ttu-id="83592-137">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="83592-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="83592-138">Ve stromovém zobrazení vyberte položku nabídky, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="83592-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="83592-139">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="83592-139">Click **Edit**.</span></span>
19. <span data-ttu-id="83592-140">Klepnutím na šipku přidejte položku nabídky do nabídky.</span><span class="sxs-lookup"><span data-stu-id="83592-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="83592-141">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-141">Click **Save**.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="83592-142">Vytvoření prahové hodnoty inventury</span><span class="sxs-lookup"><span data-stu-id="83592-142">Create a counting threshold</span></span>
1. <span data-ttu-id="83592-143">V **navigačním podokně** přejděte na **Moduly > řízení skladu > Nastavení > Cyklická inventura > Prahové hodnoty cyklické inventury**.</span><span class="sxs-lookup"><span data-stu-id="83592-143">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count thresholds**.</span></span>
2. <span data-ttu-id="83592-144">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-144">Click **New**.</span></span>
3. <span data-ttu-id="83592-145">Zadejte hodnotu do pole **ID prahové hodnoty cyklické inventury**.</span><span class="sxs-lookup"><span data-stu-id="83592-145">In the **Cycle counting threshold ID** field, type a value.</span></span>
4. <span data-ttu-id="83592-146">Nastavte možnost **Ihned zpracovat cyklickou inventuru** na Ano.</span><span class="sxs-lookup"><span data-stu-id="83592-146">Set the **Process cycle counting immediately** option to Yes.</span></span>
5. <span data-ttu-id="83592-147">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="83592-147">In the **Description** field, type a value.</span></span>
6. <span data-ttu-id="83592-148">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-148">Click **Save**.</span></span>
7. <span data-ttu-id="83592-149">Klikněte na **Vybrat umístění**.</span><span class="sxs-lookup"><span data-stu-id="83592-149">Click **Select locations**.</span></span>
8. <span data-ttu-id="83592-150">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="83592-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="83592-151">V poli **Kritéria** vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="83592-151">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="83592-152">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="83592-152">Click **OK**.</span></span>
11. <span data-ttu-id="83592-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83592-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="83592-154">Vytvoření plánu cyklické inventury</span><span class="sxs-lookup"><span data-stu-id="83592-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="83592-155">V **navigačním podokně** přejděte na **Moduly > řízení skladu > Nastavení > Cyklická inventura > Plány cyklické inventury**.</span><span class="sxs-lookup"><span data-stu-id="83592-155">In the **Navigation pane**, go to **Modules > Warehouse management > Setup > Cycle counting > Cycle count plans**.</span></span>
2. <span data-ttu-id="83592-156">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-156">Click **New**.</span></span>
3. <span data-ttu-id="83592-157">Zadejte hodnotu do pole **ID plánu cyklické inventury**.</span><span class="sxs-lookup"><span data-stu-id="83592-157">In the **Cycle counting plan ID** field, type a value.</span></span>
4. <span data-ttu-id="83592-158">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="83592-158">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="83592-159">Do pole **Maximální počet cyklických inventur** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="83592-159">In the **Maximum number of cycle counts** field, enter a number.</span></span>
6. <span data-ttu-id="83592-160">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-160">Click **Save**.</span></span>
7. <span data-ttu-id="83592-161">Klikněte na **Vybrat umístění**.</span><span class="sxs-lookup"><span data-stu-id="83592-161">Click **Select locations**.</span></span>
8. <span data-ttu-id="83592-162">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="83592-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="83592-163">V poli **Kritéria** vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="83592-163">In the **Criteria** field, select a value.</span></span>
10. <span data-ttu-id="83592-164">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="83592-164">Click **OK**.</span></span>
11. <span data-ttu-id="83592-165">Do pole **Dny mezi cyklickými inventurami** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="83592-165">In the **Days between cycle counting** field, enter a number.</span></span> <span data-ttu-id="83592-166">Pokud je například hodnota zadaná v poli **Dny mezi cyklickými inventurami** nastavena na 5, práce cyklické inventury bude vytvořena každých pět dní.</span><span class="sxs-lookup"><span data-stu-id="83592-166">For example, if the **Days between cycle counting** field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="83592-167">Pokud je však práce cyklické inventury zpracovávána třetího dne, další práce cyklické inventury bude vytvořen pět dnů po zpracování poslední cyklické inventury, osmého dne.</span><span class="sxs-lookup"><span data-stu-id="83592-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="83592-168">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-168">Click **Save**.</span></span>
13. <span data-ttu-id="83592-169">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="83592-169">Click **New**.</span></span>
14. <span data-ttu-id="83592-170">V poli **Pořadové číslo** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="83592-170">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="83592-171">Pořadí je od nejnižšího čísla po nejvyšší číslo.</span><span class="sxs-lookup"><span data-stu-id="83592-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="83592-172">Hodnota musí být větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="83592-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="83592-173">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="83592-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="83592-174">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="83592-174">In the **Description** field, type a value.</span></span>
17. <span data-ttu-id="83592-175">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="83592-175">Click **Save**.</span></span>
18. <span data-ttu-id="83592-176">Klikněte na **Definovat dotaz na produkt**.</span><span class="sxs-lookup"><span data-stu-id="83592-176">Click **Define product** query.</span></span>
19. <span data-ttu-id="83592-177">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="83592-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="83592-178">V poli **Kritéria** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="83592-178">In the **Criteria** field, enter or select a value.</span></span>
21. <span data-ttu-id="83592-179">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="83592-179">Click **OK**.</span></span>
22. <span data-ttu-id="83592-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="83592-180">Close the page.</span></span>

