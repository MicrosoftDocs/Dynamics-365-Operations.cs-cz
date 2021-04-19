---
title: Nastavení dopravců
description: Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.
author: ShylaThompson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c292470e6c70af4dfe11bbe324ebcf93438e29d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840454"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="9580e-103">Nastavení dopravců</span><span class="sxs-lookup"><span data-stu-id="9580e-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9580e-104">Toto téma popisuje, jak nastavit dopravce a definujte podrobnosti například pro službu, způsob dodávky, úhradu přepravy, omezení přepravy nebo sazbu expedice.</span><span class="sxs-lookup"><span data-stu-id="9580e-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="9580e-105">Koordinátor přepravy potom může přiřadit dopravce k příchozímu nebo odchozímu vytížení.</span><span class="sxs-lookup"><span data-stu-id="9580e-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="9580e-106">Vytvoření nového dopravce</span><span class="sxs-lookup"><span data-stu-id="9580e-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="9580e-107">Přejděte na **Navigační > podokno Moduly > Správa přepravy > Nastavení > Dopravci > Dopravci.**</span><span class="sxs-lookup"><span data-stu-id="9580e-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="9580e-108">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9580e-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="9580e-109">Zadejte hodnotu do pole **Dopravce dodávky**.</span><span class="sxs-lookup"><span data-stu-id="9580e-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="9580e-110">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="9580e-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9580e-111">V poli **Režim** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="9580e-112">Zadání obecných informací pro dopravce</span><span class="sxs-lookup"><span data-stu-id="9580e-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="9580e-113">Přepněte rozšíření oddílu **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="9580e-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="9580e-114">Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat dopravce**.</span><span class="sxs-lookup"><span data-stu-id="9580e-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="9580e-115">V poli **Účet dodavatele** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="9580e-116">Vyberte účet dodavatele, ke kterému chcete přiřadit dopravce.</span><span class="sxs-lookup"><span data-stu-id="9580e-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="9580e-117">V poli **Typ úhrady přepravy** vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="9580e-118">Vyberte **Ručně**, pokud chcete použít stránku Úhrada přepravy, nebo vyberte **EDI** a nechte aktualizovat úhrady pomocí služby Electronic Data Interchange (EDI).</span><span class="sxs-lookup"><span data-stu-id="9580e-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="9580e-119">Zaškrtněte nebo zrušte zaškrtnutí políčka **Aktivovat hodnocení dopravce**.</span><span class="sxs-lookup"><span data-stu-id="9580e-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="9580e-120">Vytvoření nezbytných služeb pro dopravce</span><span class="sxs-lookup"><span data-stu-id="9580e-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="9580e-121">Přepněte rozšíření oddílu **Služby**.</span><span class="sxs-lookup"><span data-stu-id="9580e-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="9580e-122">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9580e-122">Select **New**.</span></span>
3. <span data-ttu-id="9580e-123">Zadejte hodnotu do pole **Služba dopravce**.</span><span class="sxs-lookup"><span data-stu-id="9580e-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="9580e-124">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="9580e-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9580e-125">V poli **Metoda přepravy** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="9580e-126">Nastavení adresy pro dopravce (volitelné)</span><span class="sxs-lookup"><span data-stu-id="9580e-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="9580e-127">Přepněte rozšíření oddílu **Adresy**.</span><span class="sxs-lookup"><span data-stu-id="9580e-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="9580e-128">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9580e-128">Select **New**.</span></span>
3. <span data-ttu-id="9580e-129">Zadejte hodnotu do pole **Název nebo popis**.</span><span class="sxs-lookup"><span data-stu-id="9580e-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="9580e-130">V poli **Země/oblast** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="9580e-131">V poli **PSČ** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="9580e-132">Zadejte hodnotu do pole **Ulice**.</span><span class="sxs-lookup"><span data-stu-id="9580e-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="9580e-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9580e-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="9580e-134">Nastavení profilu hodnocení pro dopravce</span><span class="sxs-lookup"><span data-stu-id="9580e-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="9580e-135">Rozbalte oddíl **Profily sazeb**.</span><span class="sxs-lookup"><span data-stu-id="9580e-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="9580e-136">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="9580e-136">Select **New**.</span></span>
3. <span data-ttu-id="9580e-137">Zadejte hodnotu do pole **Profil sazeb**.</span><span class="sxs-lookup"><span data-stu-id="9580e-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="9580e-138">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="9580e-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="9580e-139">V poli **Pracoviště** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="9580e-140">V poli **Sklad** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="9580e-141">V poli **Výpočet přepravních sazeb** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="9580e-142">Vyberte modul sazeb, který je v souladu se smlouvou, které máte s dopravcem.</span><span class="sxs-lookup"><span data-stu-id="9580e-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="9580e-143">V poli **Hlavní sazba** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="9580e-144">V poli **Modul mezioperačního času** vyberte z rozevírací nabídky požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="9580e-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="9580e-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9580e-145">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]