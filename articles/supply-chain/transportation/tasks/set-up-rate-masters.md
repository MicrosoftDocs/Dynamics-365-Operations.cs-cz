---
title: Nastavení hlavních sazeb
description: Tento postup popisuje, jak nastavíte hlavní sazby.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4cca9fd47a5d8c81d7b8a913d0a467bc113b584
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2020
ms.locfileid: "4424275"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="dd373-103">Nastavení hlavních sazeb</span><span class="sxs-lookup"><span data-stu-id="dd373-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd373-104">Tento postup popisuje, jak nastavíte hlavní sazby.</span><span class="sxs-lookup"><span data-stu-id="dd373-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="dd373-105">Hlavní sazby obvykle nastavuje manažer logistiky v závislosti na smlouvách podepsaných s dopravci.</span><span class="sxs-lookup"><span data-stu-id="dd373-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="dd373-106">V tomto scénáři nastavíte hlavní sazbu pro leteckého dopravce.</span><span class="sxs-lookup"><span data-stu-id="dd373-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="dd373-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="dd373-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="dd373-108">Nastavení hlavního přerušení</span><span class="sxs-lookup"><span data-stu-id="dd373-108">Set up break master</span></span>

1. <span data-ttu-id="dd373-109">Přejděte do nabídky **Správa přepravy > Nastavení > Ohodnocení > Hlavní přerušení**.</span><span class="sxs-lookup"><span data-stu-id="dd373-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="dd373-110">Hlavní změny slouží k definování struktury cen a použitých zarážek.</span><span class="sxs-lookup"><span data-stu-id="dd373-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="dd373-111">Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.</span><span class="sxs-lookup"><span data-stu-id="dd373-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="dd373-112">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd373-112">Select **New**.</span></span>
1. <span data-ttu-id="dd373-113">V poli **Hlavní přerušení** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dd373-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="dd373-114">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="dd373-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="dd373-115">V poli **Datový typ** vyberte datový typ.</span><span class="sxs-lookup"><span data-stu-id="dd373-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="dd373-116">V poli **Srovnání** zadejte požadovaný druh srovnání (pomocí operátorů).</span><span class="sxs-lookup"><span data-stu-id="dd373-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="dd373-117">Do pole **Jednotka přerušení** zadejte jednotku přerušení.</span><span class="sxs-lookup"><span data-stu-id="dd373-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="dd373-118">V sekci **Podrobnosti** vytvořte tolik přerušení, kolik je potřeba pro strukturu cen.</span><span class="sxs-lookup"><span data-stu-id="dd373-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="dd373-119">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dd373-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="dd373-120">Nastavení hlavní sazby</span><span class="sxs-lookup"><span data-stu-id="dd373-120">Set up rate master</span></span>

1. <span data-ttu-id="dd373-121">Přejděte do nabídky **Správa přepravy > Nastavení > Ohodnocení > Hlavní sazba**.</span><span class="sxs-lookup"><span data-stu-id="dd373-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="dd373-122">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd373-122">Select **New**.</span></span>
1. <span data-ttu-id="dd373-123">Zadejte hodnotu do pole **Hlavní sazba**.</span><span class="sxs-lookup"><span data-stu-id="dd373-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="dd373-124">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="dd373-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="dd373-125">V poli **ID metadat sazeb** výběrem rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dd373-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="dd373-126">ID metadat sazeb určí data potřebná pro hlavní sazbu, protože definuje metadata očekávaná modulem systému přepravy, který používá tuto hlavní sazbu.</span><span class="sxs-lookup"><span data-stu-id="dd373-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="dd373-127">V tomto příkladu vyberte možnost P2P.</span><span class="sxs-lookup"><span data-stu-id="dd373-127">For this example, select the P2P option.</span></span> <span data-ttu-id="dd373-128">To je již definováno v ukázkových datech.</span><span class="sxs-lookup"><span data-stu-id="dd373-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="dd373-129">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dd373-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="dd373-130">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dd373-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="dd373-131">Nastavení základní sazby</span><span class="sxs-lookup"><span data-stu-id="dd373-131">Set up rate base</span></span>

1. <span data-ttu-id="dd373-132">Vyberte **základní sazbu**.</span><span class="sxs-lookup"><span data-stu-id="dd373-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="dd373-133">Nastavení základní sazby určuje sazbu dopravce a slouží k nastavení struktury sazby, protože definuje strukturu kurzů v zarážkách definovaných ve hlavní změně.</span><span class="sxs-lookup"><span data-stu-id="dd373-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="dd373-134">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd373-134">Select **New**.</span></span>
3. <span data-ttu-id="dd373-135">Zadejte hodnotu do pole **Základní sazba**.</span><span class="sxs-lookup"><span data-stu-id="dd373-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="dd373-136">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="dd373-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="dd373-137">V poli **Hlavní přerušení** výběrem tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dd373-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="dd373-138">Hlavní změny slouží k definování struktury cen a použitých zarážek.</span><span class="sxs-lookup"><span data-stu-id="dd373-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="dd373-139">Cenové struktury používají vrstvené ceny vycházející z fyzických rozměrů.</span><span class="sxs-lookup"><span data-stu-id="dd373-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="dd373-140">V tomto příkladu použijte hmotnost.</span><span class="sxs-lookup"><span data-stu-id="dd373-140">For this example, use weight.</span></span> <span data-ttu-id="dd373-141">To je již definováno v ukázkových datech.</span><span class="sxs-lookup"><span data-stu-id="dd373-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="dd373-142">Vyberte odkaz na zvýrazněném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dd373-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="dd373-143">Rozbalte sekci **Podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="dd373-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="dd373-144">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd373-144">Select **New**.</span></span>
10. <span data-ttu-id="dd373-145">V poli **PSČ místa vyložení – od** zadejte „30301“.</span><span class="sxs-lookup"><span data-stu-id="dd373-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="dd373-146">V poli **PSČ místa vyložení – do** zadejte „30318“.</span><span class="sxs-lookup"><span data-stu-id="dd373-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="dd373-147">V poli **Země/oblast vyložení** zadejte „USA“ .</span><span class="sxs-lookup"><span data-stu-id="dd373-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="dd373-148">Do pole **<1,00 libry** zadejte hodnotu „100“.</span><span class="sxs-lookup"><span data-stu-id="dd373-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="dd373-149">Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 1 libra.</span><span class="sxs-lookup"><span data-stu-id="dd373-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="dd373-150">Do pole **<5,00 libry** zadejte hodnotu „300“.</span><span class="sxs-lookup"><span data-stu-id="dd373-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="dd373-151">Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 5 liber.</span><span class="sxs-lookup"><span data-stu-id="dd373-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="dd373-152">Do pole **<20,00 libry** zadejte hodnotu „500“.</span><span class="sxs-lookup"><span data-stu-id="dd373-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="dd373-153">Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 20 liber.</span><span class="sxs-lookup"><span data-stu-id="dd373-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="dd373-154">Do pole **<100,00 libry** zadejte hodnotu „1000“.</span><span class="sxs-lookup"><span data-stu-id="dd373-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="dd373-155">Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 100 liber.</span><span class="sxs-lookup"><span data-stu-id="dd373-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="dd373-156">Do pole **<1.000,00 libry** zadejte hodnotu „3000“.</span><span class="sxs-lookup"><span data-stu-id="dd373-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="dd373-157">Vložte sazbu za libru, pokud je celková hmotnost vytížení nižší než 1000 liber.</span><span class="sxs-lookup"><span data-stu-id="dd373-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="dd373-158">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dd373-158">Select **Save**.</span></span>
19. <span data-ttu-id="dd373-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dd373-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="dd373-160">Přiřazení základní sazby</span><span class="sxs-lookup"><span data-stu-id="dd373-160">Assign rate base</span></span>

1. <span data-ttu-id="dd373-161">Rozbalte část **Přiřazení základní sazby**.</span><span class="sxs-lookup"><span data-stu-id="dd373-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="dd373-162">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd373-162">Select **New**.</span></span>
    * <span data-ttu-id="dd373-163">Můžete mít několik přiřazení základní sazby pro jednotlivé hlavní sazby.</span><span class="sxs-lookup"><span data-stu-id="dd373-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="dd373-164">Díky tomu lze vytvořit několik různých cenových bodů pro každého dopravce v závislosti na cílech, službách nebo jiných základech sazby.</span><span class="sxs-lookup"><span data-stu-id="dd373-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="dd373-165">V tomto postupu můžete vytvořit pouze jedno přiřazení základní sazby.</span><span class="sxs-lookup"><span data-stu-id="dd373-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="dd373-166">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="dd373-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="dd373-167">V poli **Základní sazba** volbou tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dd373-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dd373-168">Vyberte odkaz na zvýrazněném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dd373-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="dd373-169">V poli **Služba** vyberte tlačítko rozevíracího seznamu a otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dd373-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dd373-170">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dd373-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="dd373-171">Vyberte odkaz na zvýrazněném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dd373-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="dd373-172">Do pole **PSČ pro vyzvednutí** zadejte „98052“.</span><span class="sxs-lookup"><span data-stu-id="dd373-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="dd373-173">Určete, pro které PSČ toto přiřazení základní sazby bude platné.</span><span class="sxs-lookup"><span data-stu-id="dd373-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="dd373-174">Do pole **Země/oblast pro vyzvednutí** zadejte „USA“.</span><span class="sxs-lookup"><span data-stu-id="dd373-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="dd373-175">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dd373-175">Select **Save**.</span></span>
