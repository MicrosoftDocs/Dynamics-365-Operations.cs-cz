---
title: Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby
description: Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4424188"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="bc748-103">Přidružení indexu paliva k dopravci jako nákladů na dodatečné služby</span><span class="sxs-lookup"><span data-stu-id="bc748-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc748-104">Tento průvodce popisuje vytvoření přiřazení doplňkové služby, nákladů na dodatečné služby dopravce, hlavní dodatečné služby pro palivový příplatek a přidružení dopravce index paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="bc748-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="bc748-105">Je nutné nastavit index paliva dopravce před spuštěním tohoto průvodce.</span><span class="sxs-lookup"><span data-stu-id="bc748-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="bc748-106">K tomu můžete použít postup "Nastavení indexu paliva dopravce".</span><span class="sxs-lookup"><span data-stu-id="bc748-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="bc748-107">Tyto úlohy nastavení jsou obvykle prováděny manažerem logistiky.</span><span class="sxs-lookup"><span data-stu-id="bc748-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="bc748-108">Jako ukázková data pro tento postup slouží data USMF.</span><span class="sxs-lookup"><span data-stu-id="bc748-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="bc748-109">Vytvoření hlavní dodatečné služby</span><span class="sxs-lookup"><span data-stu-id="bc748-109">Create an accessorial master</span></span>
1. <span data-ttu-id="bc748-110">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Hlavní dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="bc748-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="bc748-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc748-111">Click New.</span></span>
3. <span data-ttu-id="bc748-112">Zadejte hodnotu do pole Hlavní dodatečná služba.</span><span class="sxs-lookup"><span data-stu-id="bc748-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="bc748-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="bc748-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="bc748-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bc748-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="bc748-115">Vytvoření nákladů na dodatečné služby dopravce</span><span class="sxs-lookup"><span data-stu-id="bc748-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="bc748-116">Přejděte do nabídky Správa přepravy > Nastavení > Ohodnocení > Náklady na dodatečné služby dopravce.</span><span class="sxs-lookup"><span data-stu-id="bc748-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="bc748-117">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc748-117">Click New.</span></span>
3. <span data-ttu-id="bc748-118">Zadejte hodnotu do pole ID dodatečné služby dopravce.</span><span class="sxs-lookup"><span data-stu-id="bc748-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="bc748-119">V poli Dopravce dodávky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc748-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bc748-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bc748-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bc748-121">V tomto příkladu vyberte Dopravce s nákladními vozy.</span><span class="sxs-lookup"><span data-stu-id="bc748-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="bc748-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bc748-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bc748-123">V poli Služba dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc748-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bc748-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bc748-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bc748-125">V poli Hlavní dodatečná služba kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc748-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bc748-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bc748-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bc748-127">V tomto příkladu vyberte nově vytvořenou hlavní dodatečnou službu.</span><span class="sxs-lookup"><span data-stu-id="bc748-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="bc748-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bc748-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="bc748-129">Vytvoření přiřazení doplňkové služby</span><span class="sxs-lookup"><span data-stu-id="bc748-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="bc748-130">Klikněte na možnost Přiřazení dodatečných služeb.</span><span class="sxs-lookup"><span data-stu-id="bc748-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="bc748-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bc748-131">Click New.</span></span>
3. <span data-ttu-id="bc748-132">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="bc748-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bc748-133">Přepněte rozšíření oddílu Kritéria.</span><span class="sxs-lookup"><span data-stu-id="bc748-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="bc748-134">U kritéria můžete zvolit, aby se vždy použil palivový příplatek, nebo v tomto příkladu zvolte, aby byl použit jen v určité oblasti.</span><span class="sxs-lookup"><span data-stu-id="bc748-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="bc748-135">V poli PSČ původního místa zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bc748-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="bc748-136">V poli PSČ místa určení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bc748-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="bc748-137">Přepněte rozšíření oddílu Výpočet.</span><span class="sxs-lookup"><span data-stu-id="bc748-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="bc748-138">V části pro kalkulaci můžete určit způsob výpočtu palivového příplatku.</span><span class="sxs-lookup"><span data-stu-id="bc748-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="bc748-139">Tento výpočet závisí na jednotce dodatečné služby, kterou jste vybrali jako základ výpočtu.</span><span class="sxs-lookup"><span data-stu-id="bc748-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="bc748-140">V poli Typ poplatku za dodatečné služby vyberte „Palivový příplatek“.</span><span class="sxs-lookup"><span data-stu-id="bc748-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="bc748-141">Vyberte možnost Vzdálenost v poli Jednotka dodatečné služby.</span><span class="sxs-lookup"><span data-stu-id="bc748-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="bc748-142">V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc748-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bc748-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bc748-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bc748-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bc748-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="bc748-145">Aktualizace profilu hodnocení dopravce</span><span class="sxs-lookup"><span data-stu-id="bc748-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="bc748-146">Přejděte do nabídky Správa přepravy > Nastavení > Dopravci > Dopravci.</span><span class="sxs-lookup"><span data-stu-id="bc748-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="bc748-147">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bc748-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bc748-148">Rozbalte oddíl Profily sazeb.</span><span class="sxs-lookup"><span data-stu-id="bc748-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="bc748-149">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="bc748-149">Click Edit.</span></span>
5. <span data-ttu-id="bc748-150">V poli Index paliva dopravce kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bc748-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bc748-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bc748-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bc748-152">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bc748-152">Click Save.</span></span>

