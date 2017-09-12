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
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="96542-103">Konfigurace umístění ve skladu s povolenými procesy řízení skladu</span><span class="sxs-lookup"><span data-stu-id="96542-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96542-104">Tento průvodce popisuje konfiguraci skladového místa pro nový sklad WMS (sklad, který používá procesy rozšířené správy skladu).</span><span class="sxs-lookup"><span data-stu-id="96542-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="96542-105">Proces obvykle provádějí vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="96542-106">Tohoto průvodce můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="96542-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="96542-107">Předpokladem je, že máte nakonfigurován alespoň jeden site.</span><span class="sxs-lookup"><span data-stu-id="96542-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="96542-108">Vytvoření nového skladu</span><span class="sxs-lookup"><span data-stu-id="96542-108">Create a new warehouse</span></span>
1. <span data-ttu-id="96542-109">Přejděte do nabídky Sklady.</span><span class="sxs-lookup"><span data-stu-id="96542-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="96542-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-110">Click New.</span></span>
3. <span data-ttu-id="96542-111">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="96542-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="96542-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="96542-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="96542-113">Zadejte hodnotu do pole Pracoviště.</span><span class="sxs-lookup"><span data-stu-id="96542-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="96542-114">Rozbalte nebo sbalte oddíl Sklad.</span><span class="sxs-lookup"><span data-stu-id="96542-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="96542-115">Vyberte pro možnost Použít procesy řízení skladu nastavení Ano.</span><span class="sxs-lookup"><span data-stu-id="96542-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="96542-116">Toto nastavení umožňuje spustit rozšířené skladové procesy prostřednictvím skladové práce a mobilních zařízení.</span><span class="sxs-lookup"><span data-stu-id="96542-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="96542-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="96542-118">Definování formátu skladového místa</span><span class="sxs-lookup"><span data-stu-id="96542-118">Define a location format</span></span>
1. <span data-ttu-id="96542-119">Přejděte do nabídky Formáty skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-119">Go to Location formats.</span></span>
    * <span data-ttu-id="96542-120">Formáty skladového místa představují systém pojmenování pro vytváření jedinečných a konzistentních názvů pro pozice přihrádky skladového místa používané ve skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="96542-121">Může být užitečný při použití oddělovačů ve formátu skladového místa pro usnadnění identifikace součástí skladového místa, například číslo uličky.</span><span class="sxs-lookup"><span data-stu-id="96542-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="96542-122">V tomto příkladu vytvoříte název se čtyřmi součástmi.</span><span class="sxs-lookup"><span data-stu-id="96542-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="96542-123">Může to být například ulička, stojan, police a přihrádka.</span><span class="sxs-lookup"><span data-stu-id="96542-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="96542-124">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-124">Click New.</span></span>
3. <span data-ttu-id="96542-125">Zadejte hodnotu do pole Formát skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="96542-126">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="96542-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="96542-127">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="96542-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="96542-128">Popisuje, co představuje první součást názvu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="96542-129">Může to být například ulička.</span><span class="sxs-lookup"><span data-stu-id="96542-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="96542-130">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="96542-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="96542-131">Určuje, kolik znaků musí mít tato část názvu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="96542-132">Součet všech součástí v názvu, včetně oddělovačů, nesmí překročit 10 znaků.</span><span class="sxs-lookup"><span data-stu-id="96542-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="96542-133">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="96542-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="96542-134">Určuje, jaký znak nebo symbol bude použit mezi první a druhou součástí názvu.</span><span class="sxs-lookup"><span data-stu-id="96542-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="96542-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-135">Click New.</span></span>
9. <span data-ttu-id="96542-136">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="96542-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="96542-137">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="96542-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="96542-138">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="96542-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="96542-139">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="96542-139">Click New.</span></span>
13. <span data-ttu-id="96542-140">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="96542-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="96542-141">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="96542-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="96542-142">Zadejte hodnotu do pole Oddělovač.</span><span class="sxs-lookup"><span data-stu-id="96542-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="96542-143">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="96542-143">Click New.</span></span>
17. <span data-ttu-id="96542-144">Zadejte hodnotu do pole Popis segmentu.</span><span class="sxs-lookup"><span data-stu-id="96542-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="96542-145">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="96542-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="96542-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="96542-146">Click Save.</span></span>
20. <span data-ttu-id="96542-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="96542-148">Definování typů skladových míst</span><span class="sxs-lookup"><span data-stu-id="96542-148">Define location types</span></span>
1. <span data-ttu-id="96542-149">Přejděte do nabídky Typy skladových míst.</span><span class="sxs-lookup"><span data-stu-id="96542-149">Go to Location types.</span></span>
    * <span data-ttu-id="96542-150">Typy skladových míst lze použít jako možnosti filtrování k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="96542-151">Minimální podmínkou pro možnost definování procesu správy výstupního skladu je vytvoření typů přechodných a konečných skladových míst.</span><span class="sxs-lookup"><span data-stu-id="96542-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="96542-152">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-152">Click New.</span></span>
3. <span data-ttu-id="96542-153">Zadejte hodnotu do pole Typ místa.</span><span class="sxs-lookup"><span data-stu-id="96542-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="96542-154">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="96542-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="96542-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="96542-156">Definování profilu skladového místa</span><span class="sxs-lookup"><span data-stu-id="96542-156">Define location profile</span></span>
1. <span data-ttu-id="96542-157">Přejděte do nabídky Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="96542-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="96542-158">Definování profilů skladových míst je velmi důležité.</span><span class="sxs-lookup"><span data-stu-id="96542-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="96542-159">Zde lze spravovat kapacitu seskupených skladových míst a také zásady týkající se toho, jaké zásoby budou uloženy a jak jsou uloženy.</span><span class="sxs-lookup"><span data-stu-id="96542-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="96542-160">Profily skladového místa lze použít jako možnosti filtrování k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="96542-161">Je nutné vytvořit profil skladového místa uživatele, chcete-li povolit procesy správy skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="96542-162">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-162">Click New.</span></span>
3. <span data-ttu-id="96542-163">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="96542-164">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="96542-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="96542-165">V poli Formát skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96542-166">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="96542-167">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96542-168">V poli Typ skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="96542-169">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="96542-170">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="96542-171">Zaškrtněte nebo zrušte zaškrtnutí políčka Povolit smíšené stavy zásob.</span><span class="sxs-lookup"><span data-stu-id="96542-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="96542-172">Tuto možnost povolte, pokud chcete povolit hodnoty smíšeného stavu zásob ve skladových místech, které budou seskupeny podle tohoto profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="96542-173">Zaškrtněte nebo zrušte zaškrtnutí políčka Pravidla přepisu pro dny dávky.</span><span class="sxs-lookup"><span data-stu-id="96542-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="96542-174">Tuto možnost povolte, chcete-li přepsat pravidlo pro určení, o kolik dnů se data vypršení platnosti skladové dávky mohou lišit, aby bylo možné míchat dávky skladových zásob nesplňující požadavky tohoto pravidla.</span><span class="sxs-lookup"><span data-stu-id="96542-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="96542-175">Zaškrtněte políčko Povolit cyklickou inventuru nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="96542-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="96542-176">Tuto možnost povolte, pokud chcete povolit zpracování cyklické inventury ve všech skladových místech, které budou seskupeny podle tohoto profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="96542-177">Rozbalte nebo sbalte oddíl Rozměry.</span><span class="sxs-lookup"><span data-stu-id="96542-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="96542-178">Karta Dimenze umožňuje definovat parametry a metody pro povolení přesných výpočtů kapacity vytížení v rámci každého skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="96542-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="96542-180">Povolení parametrů řízení skladu</span><span class="sxs-lookup"><span data-stu-id="96542-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="96542-181">Přejděte do nabídky Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="96542-182">Aby bylo možné zpracovat práci skladu, je nutné nastavit parametry pro profil skladového místa uživatele, typ fázování umístění a typ konečného skladového místa. Jakmile bude odchozí proces končit u typu konečného skladového místa, který definujete, související výstupní transakce budou aktualizovány na hodnotu Vydáno.</span><span class="sxs-lookup"><span data-stu-id="96542-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="96542-183">Rozbalte nebo sbalte oddíl Profily umístění.</span><span class="sxs-lookup"><span data-stu-id="96542-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="96542-184">V poli Umístění uživatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="96542-185">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="96542-186">Rozbalte nebo sbalte oddíl Typy umístění.</span><span class="sxs-lookup"><span data-stu-id="96542-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="96542-187">V poli Přechodné skladové místo kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="96542-188">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96542-189">V poli Typ konečného skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="96542-190">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="96542-191">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="96542-192">Definování skupin zón skladu</span><span class="sxs-lookup"><span data-stu-id="96542-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="96542-193">Přejděte do nabídky Skupiny zón skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="96542-194">Zóny skladu lze použít jako filtry k řízení různých procesů správy skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="96542-195">Před definováním zóny je nutné vytvořit skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="96542-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="96542-196">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-196">Click New.</span></span>
3. <span data-ttu-id="96542-197">Zadejte hodnotu do pole ID skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="96542-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="96542-198">Zadejte hodnotu do pole Název skupiny zón.</span><span class="sxs-lookup"><span data-stu-id="96542-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="96542-199">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="96542-200">Definování zón skladu</span><span class="sxs-lookup"><span data-stu-id="96542-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="96542-201">Přejděte do nabídky Zóny.</span><span class="sxs-lookup"><span data-stu-id="96542-201">Go to Zones.</span></span>
2. <span data-ttu-id="96542-202">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-202">Click New.</span></span>
3. <span data-ttu-id="96542-203">Zadejte hodnotu do pole ID zóny.</span><span class="sxs-lookup"><span data-stu-id="96542-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="96542-204">Zadejte hodnotu do pole Název zóny.</span><span class="sxs-lookup"><span data-stu-id="96542-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="96542-205">V poli ID skupiny zón kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96542-206">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="96542-207">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96542-208">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="96542-209">Vytvoření skladových míst pomocí průvodce nastavením skladového místa</span><span class="sxs-lookup"><span data-stu-id="96542-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="96542-210">Přejděte do nabídky Průvodce nastavením skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="96542-211">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="96542-212">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="96542-213">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="96542-214">V poli ID zóny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96542-215">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="96542-216">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="96542-217">V poli ID profilu skladového místa kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="96542-218">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="96542-219">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="96542-220">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="96542-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="96542-221">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="96542-222">Pole Od čísla a Do čísla definují počet skladových míst, která budou vytvořena.</span><span class="sxs-lookup"><span data-stu-id="96542-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="96542-223">Například pokud nastavíte číslo Od na hodnotu 1 a Do na hodnotu 3 pro všechny čtyři řádky formátu skladového místa, vytvoří se 81 skladových míst (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="96542-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="96542-224">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="96542-225">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="96542-226">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="96542-227">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="96542-228">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="96542-229">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="96542-230">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="96542-231">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="96542-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="96542-232">Zadejte číslo do pole Od čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="96542-233">Zadejte číslo do pole Do čísla.</span><span class="sxs-lookup"><span data-stu-id="96542-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="96542-234">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="96542-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="96542-235">Ruční vytvoření skladových míst</span><span class="sxs-lookup"><span data-stu-id="96542-235">Create locations manually</span></span>
1. <span data-ttu-id="96542-236">Přejděte do nabídky Umístění.</span><span class="sxs-lookup"><span data-stu-id="96542-236">Go to Locations.</span></span>
    * <span data-ttu-id="96542-237">Lze snadno ručně vytvořit skladová místa ve skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="96542-238">Název skladového místa a ID profilu skladového místa jsou povinné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="96542-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="96542-239">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-239">Click New.</span></span>
3. <span data-ttu-id="96542-240">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="96542-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="96542-241">Zadejte hodnotu do pole Místo konání.</span><span class="sxs-lookup"><span data-stu-id="96542-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="96542-242">Všimněte si, že zde vytváříte nové skladové místo, proto je nutné zadat nový jedinečný název, ne vybírat existující název.</span><span class="sxs-lookup"><span data-stu-id="96542-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="96542-243">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="96542-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="96542-245">Definování kategorií velikosti balení</span><span class="sxs-lookup"><span data-stu-id="96542-245">Define Pack size categories</span></span>
1. <span data-ttu-id="96542-246">Přejděte do nabídky Kategorie velikosti balení.</span><span class="sxs-lookup"><span data-stu-id="96542-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="96542-247">Kategorie velikosti balení lze použít k seskupování položek, které mají podobné fyzické rozměry balení.</span><span class="sxs-lookup"><span data-stu-id="96542-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="96542-248">V tomto příkladu se použije kategorie velikosti balení k řízení kapacity při výdejních skladových místech v rámci konkrétní zóny skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="96542-249">Všimněte si, že ID kategorie velikosti balení musí být přiřazeno k entitě uvolněného produktu, aby bylo možné jej použít jako součást zpracování skladových limitů.</span><span class="sxs-lookup"><span data-stu-id="96542-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="96542-250">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-250">Click New.</span></span>
3. <span data-ttu-id="96542-251">V poli ID kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="96542-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="96542-252">V poli Název kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="96542-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="96542-253">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="96542-254">Definice limitů pro místo uskladnění</span><span class="sxs-lookup"><span data-stu-id="96542-254">Define location stocking limits</span></span>
1. <span data-ttu-id="96542-255">Přejděte do nabídky Limity pro místo uskladnění.</span><span class="sxs-lookup"><span data-stu-id="96542-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="96542-256">Limity pro místo uskladnění umožňují zajistit, aby nebyla vytvořena práce vyžadující umístění zásob na skladové místo, které nemá fyzickou kapacitu pro zásoby.</span><span class="sxs-lookup"><span data-stu-id="96542-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="96542-257">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-257">Click New.</span></span>
3. <span data-ttu-id="96542-258">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="96542-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="96542-259">Zadejte hodnotu do pole ID profilu skladového místa.</span><span class="sxs-lookup"><span data-stu-id="96542-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="96542-260">V poli ID kategorie velikosti balení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="96542-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="96542-261">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="96542-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="96542-262">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="96542-262">Click Save.</span></span>
8. <span data-ttu-id="96542-263">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="96542-264">Definování pevných výdejních skladových míst</span><span class="sxs-lookup"><span data-stu-id="96542-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="96542-265">Přejděte do nabídky Pevná skladová místa.</span><span class="sxs-lookup"><span data-stu-id="96542-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="96542-266">Můžete definovat skladová místa k použití pro produkt nebo variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="96542-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="96542-267">Je možné vytvořit více pevných skladových míst pro stejný produkt v rámci stejného skladu.</span><span class="sxs-lookup"><span data-stu-id="96542-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="96542-268">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="96542-268">Click New.</span></span>
3. <span data-ttu-id="96542-269">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="96542-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="96542-270">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="96542-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="96542-271">V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="96542-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="96542-272">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="96542-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="96542-273">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="96542-273">Close the page.</span></span>


