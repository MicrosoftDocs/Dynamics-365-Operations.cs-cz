--- 
title: "Konfigurace umístění ve skladu s povolenými procesy řízení skladu"
description: "Tento průvodce popisuje konfiguraci skladového místa pro nový sklad WMS (sklad, který používá procesy rozšířené správy skladu)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1b08cadc26f459bc197393e3794cb67bce6516d6
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="e0ba5-103">Konfigurace umístění ve skladu s povolenými procesy řízení skladu</span><span class="sxs-lookup"><span data-stu-id="e0ba5-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0ba5-104">Tento průvodce popisuje konfiguraci skladového místa pro nový sklad WMS (sklad, který používá procesy rozšířené správy skladu).</span><span class="sxs-lookup"><span data-stu-id="e0ba5-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="e0ba5-105">Proces obvykle provádějí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="e0ba5-106">Tohoto průvodce můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e0ba5-107">Předpokladem je, že máte nakonfigurován alespoň jeden site.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="e0ba5-108">Vytvoření nového skladu</span><span class="sxs-lookup"><span data-stu-id="e0ba5-108">Create a new warehouse</span></span>
1. <span data-ttu-id="e0ba5-109">Přejděte do nabídky Sklady.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="e0ba5-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-110">Click New.</span></span>
3. <span data-ttu-id="e0ba5-111">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-113">Zadejte hodnotu do pole Pracoviště.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="e0ba5-114">Rozbalte nebo sbalte oddíl Sklad.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="e0ba5-115">Vyberte pro možnost Použít procesy řízení skladu nastavení Ano.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="e0ba5-116">Toto nastavení umožňuje spustit rozšířené skladové procesy prostřednictvím skladové práce a mobilních zařízení.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="e0ba5-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="e0ba5-118">Definování formátu skladového místa</span><span class="sxs-lookup"><span data-stu-id="e0ba5-118">Define a location format</span></span>
1. <span data-ttu-id="e0ba5-119">Přejděte do nabídky Formáty skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-119">Go to Location formats.</span></span>
    * <span data-ttu-id="e0ba5-120">Formáty skladového místa představují systém pojmenování pro vytváření jedinečných a konzistentních názvů pro pozice přihrádky skladového místa používané ve skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="e0ba5-121">Může být užitečný při použití oddělovačů ve formátu skladového místa pro usnadnění identifikace součástí skladového místa, například číslo uličky.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="e0ba5-122">V tomto příkladu vytvoříte název se čtyřmi součástmi.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="e0ba5-123">Může to být například ulička, stojan, police a přihrádka.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="e0ba5-124">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-124">Click New.</span></span>
3. <span data-ttu-id="e0ba5-125">Zadejte hodnotu do pole Formát skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-126">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-127">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="e0ba5-128">Popisuje, co představuje první součást názvu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="e0ba5-129">Může to být například ulička.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="e0ba5-130">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="e0ba5-131">Určuje, kolik znaků musí mít tato část názvu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="e0ba5-132">Součet všech součástí v názvu, včetně oddělovačů, nesmí překročit 10 znaků.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="e0ba5-133">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="e0ba5-134">Určuje, jaký znak nebo symbol bude použit mezi první a druhou součástí názvu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="e0ba5-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-135">Click New.</span></span>
9. <span data-ttu-id="e0ba5-136">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="e0ba5-137">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="e0ba5-138">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="e0ba5-139">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-139">Click New.</span></span>
13. <span data-ttu-id="e0ba5-140">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="e0ba5-141">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="e0ba5-142">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="e0ba5-143">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-143">Click New.</span></span>
17. <span data-ttu-id="e0ba5-144">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="e0ba5-145">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="e0ba5-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-146">Click Save.</span></span>
20. <span data-ttu-id="e0ba5-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="e0ba5-148">Definování typů skladových míst</span><span class="sxs-lookup"><span data-stu-id="e0ba5-148">Define location types</span></span>
1. <span data-ttu-id="e0ba5-149">Přejděte do nabídky Typy skladových míst.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-149">Go to Location types.</span></span>
    * <span data-ttu-id="e0ba5-150">Typy skladových míst lze použít jako možnosti filtrování k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="e0ba5-151">Minimální podmínkou pro možnost definování procesu správy výstupního skladu je vytvoření typů přechodných a konečných skladových míst.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="e0ba5-152">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-152">Click New.</span></span>
3. <span data-ttu-id="e0ba5-153">Zadejte hodnotu do pole Typ místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-154">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="e0ba5-156">Definování profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="e0ba5-156">Define location profile</span></span>
1. <span data-ttu-id="e0ba5-157">Přejděte do nabídky Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="e0ba5-158">Definování profilů skladových míst je velmi důležité.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="e0ba5-159">Zde lze spravovat kapacitu seskupených skladových míst a také zásady týkající se toho, jaké zásoby budou uloženy a jak jsou uloženy.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="e0ba5-160">Profily skladového místa lze použít jako možnosti filtrování k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="e0ba5-161">Je nutné vytvořit profil skladového místa uživatele, chcete-li povolit procesy správy skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="e0ba5-162">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-162">Click New.</span></span>
3. <span data-ttu-id="e0ba5-163">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-164">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-165">V poli Formát skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0ba5-166">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0ba5-167">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0ba5-168">V poli Typ skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e0ba5-169">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e0ba5-170">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e0ba5-171">Zaškrtněte nebo zrušte zaškrtnutí políčka Povolit smíšené stavy zásob.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="e0ba5-172">Tuto možnost povolte, pokud chcete povolit hodnoty smíšeného stavu zásob ve skladových místech, které budou seskupeny podle tohoto profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="e0ba5-173">Zaškrtněte nebo zrušte zaškrtnutí políčka Pravidla přepisu pro dny dávky.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="e0ba5-174">Tuto možnost povolte, chcete-li přepsat pravidlo pro určení, o kolik dnů se data vypršení platnosti skladové dávky mohou lišit, aby bylo možné míchat dávky skladových zásob nesplňující požadavky tohoto pravidla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="e0ba5-175">Zaškrtněte políčko Povolit cyklickou inventuru nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="e0ba5-176">Tuto možnost povolte, pokud chcete povolit zpracování cyklické inventury ve všech skladových místech, které budou seskupeny podle tohoto profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="e0ba5-177">Rozbalte nebo sbalte oddíl Rozměry.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="e0ba5-178">Karta Dimenze umožňuje definovat parametry a metody pro povolení přesných výpočtů kapacity vytížení v rámci každého skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="e0ba5-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="e0ba5-180">Povolení parametrů řízení skladu</span><span class="sxs-lookup"><span data-stu-id="e0ba5-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="e0ba5-181">Přejděte do nabídky Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="e0ba5-182">Aby bylo možné zpracovat práci skladu, je nutné nastavit parametry pro profil skladového místa uživatele, typ fázování umístění a typ konečného skladového místa. Jakmile bude odchozí proces končit u typu konečného skladového místa, který definujete, související výstupní transakce budou aktualizovány na hodnotu Vydáno.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="e0ba5-183">Rozbalte nebo sbalte oddíl Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="e0ba5-184">V poli Umístění uživatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e0ba5-185">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e0ba5-186">Rozbalte nebo sbalte oddíl Typy umístění.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="e0ba5-187">V poli Přechodné skladové místo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e0ba5-188">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0ba5-189">V poli Typ konečného skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e0ba5-190">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e0ba5-191">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="e0ba5-192">Definování skupin zón skladu</span><span class="sxs-lookup"><span data-stu-id="e0ba5-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="e0ba5-193">Přejděte do nabídky Skupiny zón skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="e0ba5-194">Zóny skladu lze použít jako filtry k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="e0ba5-195">Před definováním zóny je nutné vytvořit skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="e0ba5-196">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-196">Click New.</span></span>
3. <span data-ttu-id="e0ba5-197">Zadejte hodnotu do pole ID skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-198">Zadejte hodnotu do pole Název skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-199">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="e0ba5-200">Definování zón skladu</span><span class="sxs-lookup"><span data-stu-id="e0ba5-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="e0ba5-201">Přejděte do nabídky Zóny.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-201">Go to Zones.</span></span>
2. <span data-ttu-id="e0ba5-202">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-202">Click New.</span></span>
3. <span data-ttu-id="e0ba5-203">Zadejte hodnotu do pole ID zóny.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-204">Zadejte hodnotu do pole Název zóny.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-205">V poli ID skupiny zón kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0ba5-206">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0ba5-207">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0ba5-208">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="e0ba5-209">Vytvoření skladových míst pomocí průvodce nastavením skladového místa</span><span class="sxs-lookup"><span data-stu-id="e0ba5-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="e0ba5-210">Přejděte do nabídky Průvodce nastavením skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="e0ba5-211">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e0ba5-212">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e0ba5-213">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e0ba5-214">V poli ID zóny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0ba5-215">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0ba5-216">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0ba5-217">V poli ID profilu skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e0ba5-218">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e0ba5-219">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e0ba5-220">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="e0ba5-221">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="e0ba5-222">Pole Od čísla a Do čísla definují počet skladových míst, která budou vytvořena.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="e0ba5-223">Například pokud nastavíte číslo Od na hodnotu 1 a Do na hodnotu 3 pro všechny čtyři řádky formátu skladového místa, vytvoří se 81 skladových míst (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="e0ba5-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="e0ba5-224">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="e0ba5-225">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="e0ba5-226">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="e0ba5-227">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="e0ba5-228">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="e0ba5-229">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="e0ba5-230">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="e0ba5-231">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="e0ba5-232">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="e0ba5-233">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="e0ba5-234">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="e0ba5-235">Ruční vytvoření skladových míst</span><span class="sxs-lookup"><span data-stu-id="e0ba5-235">Create locations manually</span></span>
1. <span data-ttu-id="e0ba5-236">Přejděte do nabídky Umístění.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-236">Go to Locations.</span></span>
    * <span data-ttu-id="e0ba5-237">Lze snadno ručně vytvořit skladová místa ve skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="e0ba5-238">Název skladového místa a ID profilu skladového místa jsou povinné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="e0ba5-239">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-239">Click New.</span></span>
3. <span data-ttu-id="e0ba5-240">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-241">Zadejte hodnotu do pole Místo konání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="e0ba5-242">Všimněte si, že zde vytváříte nové skladové místo, proto je nutné zadat nový jedinečný název, ne vybírat existující název.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="e0ba5-243">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="e0ba5-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="e0ba5-245">Definování kategorií velikosti balení</span><span class="sxs-lookup"><span data-stu-id="e0ba5-245">Define Pack size categories</span></span>
1. <span data-ttu-id="e0ba5-246">Přejděte do nabídky Kategorie velikosti balení.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="e0ba5-247">Kategorie velikosti balení lze použít k seskupování položek, které mají podobné fyzické rozměry balení.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="e0ba5-248">V tomto příkladu se použije kategorie velikosti balení k řízení kapacity při výdejních skladových místech v rámci konkrétní zóny skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="e0ba5-249">Všimněte si, že ID kategorie velikosti balení musí být přiřazeno k entitě uvolněného produktu, aby bylo možné jej použít jako součást zpracování skladových limitů.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="e0ba5-250">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-250">Click New.</span></span>
3. <span data-ttu-id="e0ba5-251">V poli ID kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-252">V poli Název kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-253">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="e0ba5-254">Definice limitů pro místo uskladnění</span><span class="sxs-lookup"><span data-stu-id="e0ba5-254">Define location stocking limits</span></span>
1. <span data-ttu-id="e0ba5-255">Přejděte do nabídky Limity pro místo uskladnění.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="e0ba5-256">Limity pro místo uskladnění umožňují zajistit, aby nebyla vytvořena práce vyžadující umístění zásob na skladové místo, které nemá fyzickou kapacitu pro zásoby.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="e0ba5-257">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-257">Click New.</span></span>
3. <span data-ttu-id="e0ba5-258">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-259">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-260">V poli ID kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="e0ba5-261">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="e0ba5-262">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-262">Click Save.</span></span>
8. <span data-ttu-id="e0ba5-263">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="e0ba5-264">Definování pevných výdejních skladových míst</span><span class="sxs-lookup"><span data-stu-id="e0ba5-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="e0ba5-265">Přejděte do nabídky Pevná skladová místa.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="e0ba5-266">Můžete definovat skladová místa k použití pro produkt nebo variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="e0ba5-267">Je možné vytvořit více pevných skladových míst pro stejný produkt v rámci stejného skladu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="e0ba5-268">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-268">Click New.</span></span>
3. <span data-ttu-id="e0ba5-269">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="e0ba5-270">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="e0ba5-271">V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e0ba5-272">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e0ba5-273">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0ba5-273">Close the page.</span></span>


