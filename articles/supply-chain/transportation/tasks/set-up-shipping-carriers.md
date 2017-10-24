--- 
title: "Nastavení dopravců"
description: "Tento postup popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice."
author: BibiSp
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
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e27be049bebd63c9266029b8981874417a9f0a8c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="dc719-103">Nastavení dopravců</span><span class="sxs-lookup"><span data-stu-id="dc719-103">Set up shipping carriers</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc719-104">Tento postup popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.</span><span class="sxs-lookup"><span data-stu-id="dc719-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="dc719-105">Koordinátor přepravy potom může přiřadit dopravce k příchozímu nebo odchozímu vytížení.</span><span class="sxs-lookup"><span data-stu-id="dc719-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="dc719-106">Vytvoření nového dopravce</span><span class="sxs-lookup"><span data-stu-id="dc719-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="dc719-107">Přejděte do nabídky Správa přepravy > Nastavení > Dopravci > Dopravci.</span><span class="sxs-lookup"><span data-stu-id="dc719-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="dc719-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc719-108">Click New.</span></span>
3. <span data-ttu-id="dc719-109">Zadejte hodnotu do pole Dopravce dodávky .</span><span class="sxs-lookup"><span data-stu-id="dc719-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="dc719-110">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="dc719-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="dc719-111">V poli Režim kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dc719-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="dc719-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="dc719-114">Zadání obecných informací pro dopravce</span><span class="sxs-lookup"><span data-stu-id="dc719-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="dc719-115">Přepněte rozšíření oddílu Přehled.</span><span class="sxs-lookup"><span data-stu-id="dc719-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="dc719-116">Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivovat dopravce.</span><span class="sxs-lookup"><span data-stu-id="dc719-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="dc719-117">V poli Dodavatel kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="dc719-118">Vyberte účet dodavatele, ke kterému chcete přiřadit dopravce.</span><span class="sxs-lookup"><span data-stu-id="dc719-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="dc719-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="dc719-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dc719-121">V poli Typ úhrady přepravy vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="dc719-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="dc719-122">Vyberte Ručně, pokud chcete použít stránku Úhrada přepravy, nebo vyberte EDI a nechte aktualizovat úhrady pomocí služby Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="dc719-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="dc719-123">Zaškrtněte nebo zrušte zaškrtnutí políčka Aktivovat hodnocení dopravce.</span><span class="sxs-lookup"><span data-stu-id="dc719-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="dc719-124">Vytvoření nezbytných služeb pro dopravce</span><span class="sxs-lookup"><span data-stu-id="dc719-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="dc719-125">Přepněte rozšíření oddílu Služby.</span><span class="sxs-lookup"><span data-stu-id="dc719-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="dc719-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc719-126">Click New.</span></span>
3. <span data-ttu-id="dc719-127">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="dc719-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dc719-128">Zadejte hodnotu do pole Služba dopravce.</span><span class="sxs-lookup"><span data-stu-id="dc719-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="dc719-129">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="dc719-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="dc719-130">V poli Metoda přepravy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dc719-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="dc719-132">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="dc719-133">Nastavení adresy pro dopravce (volitelné)</span><span class="sxs-lookup"><span data-stu-id="dc719-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="dc719-134">Přepněte rozšíření oddílu Adresy.</span><span class="sxs-lookup"><span data-stu-id="dc719-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="dc719-135">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc719-135">Click New.</span></span>
3. <span data-ttu-id="dc719-136">Zadejte hodnotu do pole Název nebo popis.</span><span class="sxs-lookup"><span data-stu-id="dc719-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="dc719-137">V poli Země / oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="dc719-138">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="dc719-139">V poli PSČ kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dc719-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="dc719-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dc719-142">Zadejte hodnotu do pole Ulice.</span><span class="sxs-lookup"><span data-stu-id="dc719-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="dc719-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dc719-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="dc719-144">Nastavení profilu hodnocení pro dopravce</span><span class="sxs-lookup"><span data-stu-id="dc719-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="dc719-145">Rozbalte oddíl Profily sazeb.</span><span class="sxs-lookup"><span data-stu-id="dc719-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="dc719-146">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc719-146">Click New.</span></span>
3. <span data-ttu-id="dc719-147">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="dc719-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dc719-148">Zadejte hodnotu do pole Profil sazeb.</span><span class="sxs-lookup"><span data-stu-id="dc719-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="dc719-149">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="dc719-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="dc719-150">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="dc719-151">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="dc719-152">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="dc719-153">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="dc719-154">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="dc719-155">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dc719-156">V poli Výpočet přepravních sazeb kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="dc719-157">Vyberte modul sazeb, který je v souladu se smlouvou, které máte s dopravcem.</span><span class="sxs-lookup"><span data-stu-id="dc719-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="dc719-158">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="dc719-159">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="dc719-160">V poli Hlavní sazba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="dc719-161">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="dc719-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="dc719-162">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="dc719-163">V poli Modul mezioperačního času kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="dc719-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="dc719-164">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dc719-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="dc719-165">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dc719-165">Click Save.</span></span>


