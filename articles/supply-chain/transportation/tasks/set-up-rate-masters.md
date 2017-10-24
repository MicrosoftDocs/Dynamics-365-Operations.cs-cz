--- 
title: "Nastavení hlavních sazeb"
description: "Tento postup popisuje, jak nastavíte hlavní sazby."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="be947-103">Nastavení hlavních sazeb</span><span class="sxs-lookup"><span data-stu-id="be947-103">Set up rate masters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be947-104">Tento postup popisuje, jak nastavíte hlavní sazby.</span><span class="sxs-lookup"><span data-stu-id="be947-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="be947-105">Hlavní sazby obvykle nastavuje manažer logistiky v závislosti na smlouvách podepsaných s dopravci.</span><span class="sxs-lookup"><span data-stu-id="be947-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="be947-106">V tomto scénáři nastavíte hlavní sazbu pro leteckého dopravce.</span><span class="sxs-lookup"><span data-stu-id="be947-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="be947-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="be947-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="be947-108">Nastavení hlavní sazby</span><span class="sxs-lookup"><span data-stu-id="be947-108">Set up rate master</span></span>
1. <span data-ttu-id="be947-109">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní sazba.</span><span class="sxs-lookup"><span data-stu-id="be947-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="be947-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be947-110">Click New.</span></span>
3. <span data-ttu-id="be947-111">Zadejte hodnotu do pole Hlavní sazba.</span><span class="sxs-lookup"><span data-stu-id="be947-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="be947-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="be947-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="be947-113">V poli ID metadat sazeb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="be947-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be947-114">ID metadat sazeb určí data potřebná pro hlavní sazbu, protože definuje metadata očekávaná modulem systému TMS, který používá tuto hlavní sazbu.</span><span class="sxs-lookup"><span data-stu-id="be947-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="be947-115">V tomto příkladu vyberte možnost P2P.</span><span class="sxs-lookup"><span data-stu-id="be947-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="be947-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be947-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="be947-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be947-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="be947-118">Nastavení základní sazby</span><span class="sxs-lookup"><span data-stu-id="be947-118">Set up rate base</span></span>
1. <span data-ttu-id="be947-119">Klikněte na možnost Základní sazba.</span><span class="sxs-lookup"><span data-stu-id="be947-119">Click Rate base.</span></span>
    * <span data-ttu-id="be947-120">Nastavení základní sazby určuje sazbu dopravce a slouží k nastavení struktury sazby, protože definuje strukturu kurzů v zarážkách definovaných ve hlavní změně.</span><span class="sxs-lookup"><span data-stu-id="be947-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="be947-121">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be947-121">Click New.</span></span>
3. <span data-ttu-id="be947-122">Zadejte hodnotu do pole Základní sazba.</span><span class="sxs-lookup"><span data-stu-id="be947-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="be947-123">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="be947-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="be947-124">V poli Hlavní změna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="be947-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="be947-125">Hlavní změny slouží k definování struktury cen a použitých zarážek.</span><span class="sxs-lookup"><span data-stu-id="be947-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="be947-126">Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.</span><span class="sxs-lookup"><span data-stu-id="be947-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="be947-127">V tomto příkladu použijte hmotnost</span><span class="sxs-lookup"><span data-stu-id="be947-127">For this example, use weight</span></span>
7. <span data-ttu-id="be947-128">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be947-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="be947-129">Přepněte rozšíření oddílu Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="be947-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="be947-130">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="be947-130">Click New.</span></span>
10. <span data-ttu-id="be947-131">V poli PSČ místa vyložení – od zadejte „30301“.</span><span class="sxs-lookup"><span data-stu-id="be947-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="be947-132">V poli PSČ místa vyložení – do zadejte „30318“.</span><span class="sxs-lookup"><span data-stu-id="be947-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="be947-133">V poli Země/oblast vyložení zadejte „USA“ .</span><span class="sxs-lookup"><span data-stu-id="be947-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="be947-134">Do pole <1,00 libry zadejte hodnotu „100“.</span><span class="sxs-lookup"><span data-stu-id="be947-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="be947-135">Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 1 libra.</span><span class="sxs-lookup"><span data-stu-id="be947-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="be947-136">Do pole < 5,00 liber zadejte hodnotu „300“.</span><span class="sxs-lookup"><span data-stu-id="be947-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="be947-137">Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 5 liber.</span><span class="sxs-lookup"><span data-stu-id="be947-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="be947-138">Do pole < 20,00 liber zadejte hodnotu „500“.</span><span class="sxs-lookup"><span data-stu-id="be947-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="be947-139">Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 20 liber.</span><span class="sxs-lookup"><span data-stu-id="be947-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="be947-140">Do pole < 100,00 liber zadejte hodnotu „1000“.</span><span class="sxs-lookup"><span data-stu-id="be947-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="be947-141">Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 100 liber.</span><span class="sxs-lookup"><span data-stu-id="be947-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="be947-142">Do pole < 1.000,00 liber zadejte hodnotu „3000“.</span><span class="sxs-lookup"><span data-stu-id="be947-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="be947-143">Vložte sazba za libru, pokud je celková hmotnost vytížení nižší než 1000 liber.</span><span class="sxs-lookup"><span data-stu-id="be947-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="be947-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be947-144">Click Save.</span></span>
19. <span data-ttu-id="be947-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be947-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="be947-146">Přiřazení základní sazby</span><span class="sxs-lookup"><span data-stu-id="be947-146">Assign rate base</span></span>
1. <span data-ttu-id="be947-147">Rozbalte oddíl Přiřazení základní sazby.</span><span class="sxs-lookup"><span data-stu-id="be947-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="be947-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be947-148">Click New.</span></span>
    * <span data-ttu-id="be947-149">Můžete mít několik přiřazení základní sazby pro jednotlivé hlavní sazby.</span><span class="sxs-lookup"><span data-stu-id="be947-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="be947-150">Díky tomu lze vytvořit několik různých cenových bodů pro každého dopravce v závislosti na cílech, službách nebo jiných základech sazby.</span><span class="sxs-lookup"><span data-stu-id="be947-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="be947-151">V tomto postupu můžete vytvořit pouze jedno přiřazení základní sazby.</span><span class="sxs-lookup"><span data-stu-id="be947-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="be947-152">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="be947-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="be947-153">V poli Základní sazba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="be947-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="be947-154">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be947-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="be947-155">V poli Služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="be947-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="be947-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="be947-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="be947-157">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be947-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="be947-158">Do pole PSČ pro vyzvednutí PSČ zadejte „98052“.</span><span class="sxs-lookup"><span data-stu-id="be947-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="be947-159">Určete, pro které PSČ toto přiřazení základní sazby bude platné.</span><span class="sxs-lookup"><span data-stu-id="be947-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="be947-160">Do pole Země/oblast pro vyzvednutí zadejte „USA“.</span><span class="sxs-lookup"><span data-stu-id="be947-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="be947-161">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be947-161">Click Save.</span></span>


