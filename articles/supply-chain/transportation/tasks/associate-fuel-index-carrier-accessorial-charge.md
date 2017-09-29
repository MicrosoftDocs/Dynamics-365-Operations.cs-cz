--- 
title: "Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby"
description: "Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a2b8534231c5fa50b1e0f709e09d318bb8202a43
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="506db-103">Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby</span><span class="sxs-lookup"><span data-stu-id="506db-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="506db-104">Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="506db-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="506db-105">Je nutné nastavit index paliva dopravce před spuštěním tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="506db-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="506db-106">K tomu můžete použít postup Nastavení indexu paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="506db-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="506db-107">Tyto úlohy nastavení jsou obvykle prováděny manažerem logistiky.</span><span class="sxs-lookup"><span data-stu-id="506db-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="506db-108">Jako ukázková data pro tento postup slouží data USMF.</span><span class="sxs-lookup"><span data-stu-id="506db-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="506db-109">Vytvoření hlavní dodatečné služby</span><span class="sxs-lookup"><span data-stu-id="506db-109">Create an accessorial master</span></span>
1. <span data-ttu-id="506db-110">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="506db-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="506db-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="506db-111">Click New.</span></span>
3. <span data-ttu-id="506db-112">Zadejte hodnotu do pole Hlavní dodatečná služba.</span><span class="sxs-lookup"><span data-stu-id="506db-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="506db-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="506db-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="506db-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="506db-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="506db-115">Vytvoření nákladů na dodatečné služby dopravce</span><span class="sxs-lookup"><span data-stu-id="506db-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="506db-116">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Náklady na dodatečné služby dopravce.</span><span class="sxs-lookup"><span data-stu-id="506db-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="506db-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="506db-117">Click New.</span></span>
3. <span data-ttu-id="506db-118">Zadejte hodnotu do pole ID dodatečné služby dopravce.</span><span class="sxs-lookup"><span data-stu-id="506db-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="506db-119">V poli Dopravce dodávky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="506db-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="506db-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="506db-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="506db-121">V tomto příkladu vyberte Dopravce s nákladními vozy.</span><span class="sxs-lookup"><span data-stu-id="506db-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="506db-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="506db-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="506db-123">V poli Služba dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="506db-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="506db-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="506db-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="506db-125">V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="506db-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="506db-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="506db-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="506db-127">V tomto příkladu vyberte nově vytvořenou hlavní dodatečnou službu.</span><span class="sxs-lookup"><span data-stu-id="506db-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="506db-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="506db-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="506db-129">Vytvoření přiřazení doplňkové služby</span><span class="sxs-lookup"><span data-stu-id="506db-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="506db-130">Klikněte na možnost Přiřazení dodatečných služeb.</span><span class="sxs-lookup"><span data-stu-id="506db-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="506db-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="506db-131">Click New.</span></span>
3. <span data-ttu-id="506db-132">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="506db-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="506db-133">Přepněte rozšíření oddílu Kritéria.</span><span class="sxs-lookup"><span data-stu-id="506db-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="506db-134">U kritéria můžete zvolit, aby se vždy použil palivový příplatek, nebo v tomto příkladu zvolte, aby byl použit jen v určité oblasti.</span><span class="sxs-lookup"><span data-stu-id="506db-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="506db-135">V poli PSČ původního místa zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="506db-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="506db-136">V poli PSČ místa určení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="506db-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="506db-137">Přepněte rozšíření oddílu Výpočet.</span><span class="sxs-lookup"><span data-stu-id="506db-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="506db-138">V části pro kalkulaci můžete určit způsob výpočtu palivového příplatku.</span><span class="sxs-lookup"><span data-stu-id="506db-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="506db-139">Tento výpočet závisí na jednotce dodatečné služby, kterou jste vybrali jako základ výpočtu.</span><span class="sxs-lookup"><span data-stu-id="506db-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="506db-140">V poli Typ poplatku za dodatečné služby vyberte „Palivový příplatek“.</span><span class="sxs-lookup"><span data-stu-id="506db-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="506db-141">Vyberte možnost Vzdálenost v poli Jednotka dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="506db-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="506db-142">V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="506db-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="506db-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="506db-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="506db-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="506db-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="506db-145">Aktualizace profilu hodnocení dopravce</span><span class="sxs-lookup"><span data-stu-id="506db-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="506db-146">Přejděte do nabídky Správa přepravy > Nastavení > Dopravci > Dopravci.</span><span class="sxs-lookup"><span data-stu-id="506db-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="506db-147">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="506db-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="506db-148">Rozbalte oddíl Profily sazeb.</span><span class="sxs-lookup"><span data-stu-id="506db-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="506db-149">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="506db-149">Click Edit.</span></span>
5. <span data-ttu-id="506db-150">V poli Index paliva dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="506db-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="506db-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="506db-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="506db-152">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="506db-152">Click Save.</span></span>


